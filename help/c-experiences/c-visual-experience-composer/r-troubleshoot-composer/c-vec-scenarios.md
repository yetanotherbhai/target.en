---
description: The scenarios in this topic show how changes made to your page affect Target's ability to display an experience.
keywords: Recommendations
seo-description: The scenarios in this topic show how changes made to your page affect Target's ability to display an experience.
seo-title: Page Modification Scenarios
solution: Target
title: Page Modification Scenarios
topic: Premium
uuid: bb868f55-7e77-49c4-81b5-3aff5b63b827
index: y
internal: n
snippet: y
---

# Page Modification Scenarios{#page-modification-scenarios}

The scenarios in this topic show how changes made to your page affect Target's ability to display an experience.

The Target selector determines where to display an experience. If a page is modified outside of Target, the changes might affect the ability of Target to display the experience.

When using the selector, the unique class is not equivalent to the ID. The selector always works with a unique class. If no class is assigned to the element, the selector calculates the number of previous siblings which have the same tag name.

>[!NOTE]
>
>Although these scenarios use list items as examples, the concepts apply to any element.

## Scenario: Insert an element with a different class name before the selected element {#section_298F661F72384F6AB957D5885A99D822}

In this example, a new element is inserted as a sibling of the element in the Target selector.

There is a possibility that first class present on the element might be added by JavaScript. In that case, delivery fails and the action is not applied.

**Inserted element:**

```
<li class="kids-section">Kids</li>
```

**Selected:**

`<li class="women-section">Women</li>`

Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:**

The selector works as expected because `li.women-section:eq(0)` is not affected.

<table id="table_F37367FB9CB343D497B5C58E8AA1B015"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Before </th> 
   <th colname="col2" class="entry"> After </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men-section"&gt;&nbsp;Men&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women-section"&gt;Women&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     
&lt;/div&gt; 
    </codeblock> </td> 
   <td colname="col2"> <p> 
     <codeblock>
       &lt;div&nbsp;id="wrap"&gt; 
      
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
      
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
      <b>&lt;li&amp;nbsp;class="kids-section"&gt;Kids&lt;/li&gt;</b> 
      
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men-section"&gt;&nbsp;Men&lt;/li&gt; 
      
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women-section"&gt;Women&lt;/li&gt; 
      
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
      
&lt;/div&gt; 
     </codeblock> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Scenario: Insert an element with the same class name as the selected element {#section_0969B88C2F154E648D9969C8C85EF55A}

In this scenario, an attempt is made to insert a list when an item in a list is selected.

**Inserted element:**

```
<ul class="nav"> 
   <li class="item"> Sale </li> 
   <li> class="item"> Offers </li> 
</ul>
```

**Selected**

`<li class="women-section">Women</li>`

Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:**

The selector does not work, because `ul.nav:eq(0)` provides a dynamically added element. The element won't be available and the action is not applied. When a similar list item with same class is added dynamically or manually after an activity has been created, a new element at the first position is created. This breaks the selector.

<table id="table_EF89AE71A0C4434CAAF1D5BE2DB61257"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Before </th> 
   <th colname="col2" class="entry"> After (Attempted) </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men-section"&gt;&nbsp;Men&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women-section"&gt;Women&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     
&lt;/div&gt; 
    </codeblock> </td> 
   <td colname="col2"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     
&nbsp;&nbsp;&nbsp; 
     <b>&lt;ul&nbsp;class="nav"&gt; 
      
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="item"&gt;&nbsp;Sale&lt;/li&gt; 
      
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&gt;&nbsp;class="item"&gt;&nbsp;Offers&lt;/li&gt; 
      
&nbsp;&nbsp;&nbsp;&lt;/ul&gt;</b> 
     
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men-section"&gt;&nbsp;Men&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women-section"&gt;Women&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     
&lt;/div&gt; 
    </codeblock> </td> 
  </tr> 
 </tbody> 
</table>

## Scenario: Insert an element after the selected element {#section_15B07B84BEE94ED39D85BBBE0733E170}

In this scenario, a list item is inserted after the selected element.

**Inserted element:**

```
<ul class="nav"> 
   <li class="men-section"> Men Clothes</li> 
   <li class="women-section"> Women Clothes</li> 
</ul>
```

**Selected:**

`<li class="women-section">Women Shoes</li>`

Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:**

In this case, inserting a list after the list ending with the selected list item works as expected. The new element is added to the same position as the selected element relative to the parent element.

<table id="table_EFDD681BAF4346E39BBD874D2013E109"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Before </th> 
   <th colname="col2" class="entry"> After </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men"&gt;Men&nbsp;Shoes&nbsp;&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women"&gt;Women&nbsp;Shoes&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     
&lt;/div&gt; 
    </codeblock> </td> 
   <td colname="col2"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men"&gt;Men&nbsp;Shoes&nbsp;&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women"&gt;Women&nbsp;Shoes&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     
&nbsp;&nbsp;&nbsp; 
     <b>&lt;ul&nbsp;class="nav"&gt; 
      
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men-section"&gt;Men&nbsp;Clothes&lt;/li&gt; 
      
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women-section"&gt;&nbsp;Women&nbsp;Clothes&lt;/li&gt; 
      
&nbsp;&nbsp;&nbsp;&lt;/ul&gt;</b> 
     
&lt;/div&gt; 
    </codeblock> </td> 
  </tr> 
 </tbody> 
</table>

## Scenario: Remove the element immediately preceding another element {#section_F193674F04F84AA593EAA1137C880EBA}

In this scenario, the list item before the selected element is deleted.

**Removed element:**

```
<li class="men-section"> Men </li>
```

**Selected:**

`<li class="women-section">Women</li>`

Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:**

The element is successfully removed because the class of the selected item is not altered.

<table id="table_BBB8D82C848749DEBC3DC9728F58A4FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Before </th> 
   <th colname="col2" class="entry"> After </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
     <b>&lt;li&amp;nbsp;class="men-section"&gt;Men&lt;/li&gt;</b> 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women-section"&gt;Women&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     
&lt;/div&gt; 
    </codeblock> </td> 
   <td colname="col2"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women-section"&gt;Women&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     
&lt;/div&gt; 
    </codeblock> </td> 
  </tr> 
 </tbody> 
</table>

## Scenario: Remove the element immediately following another element {#section_F83B51BE54924FB58679D512DAF1EBB2}

In this scenario, the list item after the selected element is deleted.

**Removed element:**

```
<li class="kids-section">Kids</li>
```

**Selected:**

`<li class="women-section">Women</li>`

Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:**

The element is successfully removed because the class of the selected item is not altered. The removed element includes a unique class within its parent subtree.

<table id="table_BB1FEF7AF7AD4EE6B7C345AEA45F6EBF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Before </th> 
   <th colname="col2" class="entry"> After </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men-section"&gt;Men&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women-section"&gt;Women&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
     <b>&lt;li&amp;nbsp;class="kids-section"&gt;Women&lt;/li&gt;</b> 
     
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     
&lt;/div&gt; 
    </codeblock> </td> 
   <td colname="col2"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men-section"&gt;Men&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women-section"&gt;Women&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     
&lt;/div&gt; 
    </codeblock> </td> 
  </tr> 
 </tbody> 
</table>

## Scenario: Remove the selected element {#section_1989CF1E2C344CC5963084ED83C18F9C}

In this scenario, the selected list item is deleted.

**Removed element:**

```
<li class="women-shoes">Women</li>
```

**Selected:**

`<li class="women-shoes">Women</li>`

Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:**

The element is successfully removed.

<table id="table_47C83AD94DF245299329439651718C0C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Before </th> 
   <th colname="col2" class="entry"> After </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men-section"&gt;Men&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="women-shoes"&gt;Women&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     
&lt;/div&gt; 
    </codeblock> </td> 
   <td colname="col2"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men-section"&gt;Men&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     
&lt;/div&gt; 
    </codeblock> </td> 
  </tr> 
 </tbody> 
</table>

## Scenario: Rename the class of the selected element {#section_79D244C588BA452DB8E433D82B7F63EA}

In this scenario, the class of the selected list item is changed.

**Changed element:**

```
<li class="women-section">Women</li>
```

**Selected:**

`<li class="women-section">Women</li>`

Selector: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:**

The element class cannot be renamed because `class` is not found.

<table id="table_C1264628F4824DBE8210FE6DD3C4CA8F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Before </th> 
   <th colname="col2" class="entry"> After (Attempted) </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men-section"&gt;Men&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
     <b>&lt;li&amp;nbsp;class="women-section"&gt;Women&lt;/li&gt;</b> 
     
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     
&lt;/div&gt; 
    </codeblock> </td> 
   <td colname="col2"> 
    <codeblock>
      &lt;div&nbsp;id="wrap"&gt; 
     
&nbsp;&nbsp;&nbsp;&lt;ul&nbsp;class="nav"&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&nbsp;class="men-section"&gt;Men&lt;/li&gt; 
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
     <b>&lt;li&amp;nbsp;class="women-shoes"&gt;Women&lt;/li&gt;</b> 
     
&nbsp;&nbsp;&nbsp;&lt;/ul&gt; 
     
&lt;/div&gt; 
    </codeblock> </td> 
  </tr> 
 </tbody> 
</table>

