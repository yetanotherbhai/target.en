---
description: When working with recommendations product data through dynamic tag management, you must create a page load rule.
keywords: Dynamic tag management
seo-description: When working with recommendations product data through dynamic tag management, you must create a page load rule.
seo-title: Create a Page Load Rule
solution: Target
title: Create a Page Load Rule
uuid: 8607b051-649c-4c16-8239-87d7af37b539
index: y
internal: n
snippet: y
translate: y
---

# Create a Page Load Rule


>[!NOTE]
>
>Before creating a page load, you must[create your data elements](t_data_elements_recs.md#task_C5F0DF393F494D7785F656DE3FBA6AF3). 

1. In Dynamic Tag Manager, select ** `Page Load Rules` ** from the left navigation.
1. Create a rule.
       Use the following settings:
    <table id="table_DB0B8B6F54D54EC3AB61A07EB8BE6C26"> 
        <thead> 
         <tr> 
        <th colname="col1" class="entry">Element</th> 
        <th colname="col2" class="entry">Settings</th> 
         </tr> 
        </thead>
        <tbody> 
       <tr> 
       <td colname="col1">Edit Page Load Rule</td> 
       <td colname="col2">Name: " Recommendations Product Data Mbox"</td> 
         </tr> 
       <tr> 
       <td colname="col1">Conditions</td> 
        <td colname="col2"> 
        <ul id="ul_06A4EADEB0E54CDC80B114A8D9B5C307"> 
        <li id="li_5FF6C8D01ECF4CA1968DEDEC5B504DF6">Trigger rule at "Bottom of Page"</li> 
       <li id="li_0CE4EF7521F045D99A4D3C28EFD78EBE"> Identify the rule conditions that applies to the order confirmation page <p>Example: Path includes "/product-detail" applies to the template page and all product pages.</p></li> 
          </ul> </td> 
        </tr> 
        <tr> 
        <td colname="col1">Adobe Target</td> 
       <td colname="col2"> 
        <ul id="ul_3FC7D7FEAA98426BAD20A305E174DC35"> 
        <li id="li_2851E0224C954F3EB4336EC4047AB6C8"> Create an mbox around a page element <p>Select a div that will not change or be removed (like a header or footer). This is where the DTMbox executes.</p></li> 
       <li id="li_491F07E535474F129B137975125532E6">Mbox Name: "productPage"</li> 
        <li id="li_34E3CABF73FE40B6AC1D419F1A9B2732">Timeout: 1500</li> 
        <li id="li_75ADB957C27F4BC790C45BCCF18310DB"> Add three arguments adding the data elements you created earlier: 
        <ul id="ul_A840489C700642F098A223D279C0FF27">
         <li id="li_975E523ADBB542C4A4117B5735C69258">orderId = type "%" in the field and then select from dropdown.</li>
        <li id="li_D0D0B18F2D034499AE7F7E022FFE79FE">orderTotal = type "%" in the field and then select from dropdown.</li>
         <li id="li_421988BAF3FB43BB9E57F6D80CEC3FCF">productPurchasedId = type "%" in the field and then select from dropdown.</li>
        </ul></li> 
        </ul> </td> 
       </tr> 
       </tbody> 
       </table>
1. Save the rule, then click ** `Approve and Publish` **.
