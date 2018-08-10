---
description: Use the Target Visual Experience Composer (VEC) to create a Recommendations activity directly on a Target-enabled page and to modify portions of the page within Target.
keywords: Recommendations;Settings;name;objective;priority;duration;reporting settings;other metadata
seo-description: Use the Target Visual Experience Composer (VEC) to create a Recommendations activity directly on a Target-enabled page and to modify portions of the page within Target.
seo-title: Create a Recommendations Activity
solution: Target
subtopic: Recommendations
title: Create a Recommendations Activity
title_outputclass: premium
topic: Premium
uuid: 78e5f5db-b308-4d0f-a4cd-a39728764636
badge: asstes/premium.png
index: y
internal: n
snippet: y
translate: y
---

# Create a Recommendations Activity

## Create a Recommendations Activity {#task_6874328773C64C44A73F0A130AD3F96F}Use the 
<keyword>
  Target 
</keyword> 
<wintitle>
  Visual Experience Composer 
</wintitle> (VEC) to create a 
<keyword>
  Recommendations 
</keyword> activity directly on a Target-enabled page and to modify portions of the page within 
<keyword>
  Target 
</keyword>.
>1. Click ** [!UICONTROL  Create Activity] ** > ** [!UICONTROL  Recommendations] **.

>       ![](graphics/Menu_CreateActivity.png) 
>1. Specify an activity URL, and then click ** [!UICONTROL  Next] **.


>       >[!NOTE]
>       >
>       >[!DNL  Target] does not differentiate between URL protocols ( [!DNL  https] and [!DNL  http]). As a result, [!DNL  https://adobe.com] and [!DNL  http://adobe.com] both match. 


>       The activity URL is the page where the recommendations will be displayed. 

>       ![](graphics/DB_NewRecAct.png) 

>       If you prefer to use the form-based Experience Composer, select that option. See [ Form-Based Experience Composer ](https://marketing.adobe.com/resources/help/en_US/target/target/t_form_experience_composer.html). 

>       When you click [!UICONTROL  Next], the VEC opens and shows your page. You can replace a current element with recommendations, or insert recommendations. 

>       For troubleshooting information about the VEC, should you have problems, see [ Troubleshooting the Visual Experience Composer ](vec-best-pracitces-and-troubleshooting.md#reference_77743144F10143A3A89D56E116D296E4). 
>1. Click an element on your page, then if recommendations are available where that element is located, click either ** [!UICONTROL  Replace w/ Recommendations] ** or ** [!UICONTROL  Insert Recommendations] ** before or after the selected element.

>       ![](graphics/Menu_Replace-Insert.png) 

>       Replacing an element with recommendations deletes the current content and replaces it with your recommendations. 
>1. Select a page type.

>       ![](graphics/Menu_PageType.png) 
>1. Select one or more criteria.

>       Criteria are displayed as cards that show information about each criteria. By default, the [!UICONTROL  Select Criteria] screen displays criteria that are compatible with your industry vertical and the page type you selected. You can change these options to display other criteria. 


>       >[!NOTE]
>       >
>       >Not every criteria will run correctly on every page. The page or mbox must pass in ` entity.id` or ` entity.categoryId` for current item/current category recommendations to be compatible. In general, it is best to show only compatible criteria. However, if you want incompatible criteria to be available for the activity, clear the ** [!UICONTROL  Compatible] ** check box. 


>       ![](graphics/SCRN_SelectCriteria2.png) 

>       If you select multiple criteria, traffic is split evenly between the selected criteria. For example, if you have selected two criteria and your activity is designed to display default content to 20% of activity entrants, then 40% of activity entrants will see the recommendations controlled by each criteria. There is no option to change the percentages for each criteria. 
>    
>    * To search for an existing criteria (for example, if a large number of criteria cards are displayed), type in the search field until the desired criteria appears, then select the criteria and click ** [!UICONTROL  Done] **. 

>      Some criteria are supplied with [!DNL  Recommendations]. You and your team can also create your own custom criteria. 

>    * To create a new criteria, click ** [!UICONTROL  Create New] ** > ** [!UICONTROL  Create Criteria] **, then fill in the information for the new criteria. For information about creating new criteria, see [ Creating Criteria ](c_algorithms.md#task_8A9CB465F28D44899F69F38AD27352FE). 

>    * You can also group criteria into sequences. To create a new criteria sequence, click ** [!UICONTROL  Create New] ** > ** [!UICONTROL  Create Criteria Sequence] **. See [ Creating Criteria Sequences ](c_algorithms.md#task_8A9CB465F28D44899F69F38AD27352FE) for more information. 

>1. Click ** [!UICONTROL  Next] **.
>1. Select a design.

>       A design is a template that determines the look of the locations on your page. [!DNL  Target] includes several preconfigured designs. You can also create your own custom designs. For more information, see [ Create a Design ](c_design-overview.md#task_CC5BD28C364742218C1ACAF0D45E0E14) and [ Customizing a Design ](c_design-overview.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59). 

>       ![](graphics/Card_SelectDesign.png) 

>       Each design shows a graphical representation of how it will look, and icons that show how many of your live and inactive activities currently use that design. 

>    
>    * To select one or more existing designs, click the designs, then click ** [!UICONTROL  Done] **. 

>      If you selected multiple criteria, you can only select one design. 

>    * To create a custom design, click ** [!UICONTROL  Create New] **, then fill in the name and code for the new design. Click ** [!UICONTROL  Next] **, then select or upload an image and click ** [!UICONTROL  Done] ** > ** [!UICONTROL  Done] **. For information about creating a new design, see [ Create a Design ](c_design-overview.md#task_CC5BD28C364742218C1ACAF0D45E0E14). 


>1. Click ** [!UICONTROL  Next] **.

>       You have the option to add promotions to your recommendations. For more information about adding front and back promotions, see [ Adding Promotions ](t_create_recs_activity.md#task_CC5BD28C364742218C1ACAF0D45E0E14). 
>1. Click ** [!UICONTROL  Save] **.

>       The VEC screen displays the recommendation design on your page. 
>1. (Optional) Click ** [!UICONTROL  Preview] ** to see how the activity will appear to visitors.

>    [!UICONTROL  Preview] mode allows you to interact with your recommendations, much as a visitor would. 

>       When you are finished previewing your recommendations, click ** [!UICONTROL  Compose] **. 
>1. Review your recommendation in the VEC, then click ** [!UICONTROL  Next] **.

>1. Review your [!DNL  Recommendations] activity in the flow diagram and make any necessary changes.

>       ![](graphics/SCRN_Workflow.png) 

>       The flow diagram leads you through the steps of choosing the audience for the activity, setting up experiences, and specifying success metrics. From the flow diagram, you can do the following: 

>    
>    * Change the audience that will see the recommendations 


>      >[!NOTE]
>      >
>      >In addition to selecting an existing audience, you can[ create an activity-only audience ](c_audiences.md#concept_A6BADCF530ED4AE1852E677FEBE68483) or [ combine multiple audiences ](c_audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) to create ad hoc audiences rather than creating a new audience. 


>      By default, all users see the recommendations. However, you can target recommendation to a specific audience. 

>      For a [!DNL  Recommendations] activity, the control group sees the page without any recommendations. 

>    * View the criteria 

>    * Change the collection (next to the [!UICONTROL  Criteria] label) 

>    * Change the percentage of entrants who see the control experience 

>    * View the design code 

>    * Change or remove a design 


>1. Click ** [!UICONTROL  Next] ** when finished.
>1. Specify your activity settings.

>       For example, type a name (required) and objective (optional) for the activity. For information about the settings, see [ Recommendations Activity Settings ](t_create_recs_activity.md#reference_3FDA8388CEEC4159949151C1829E2FBB). 


>       >[!NOTE]
>       >
>       >If you specify a [!DNL  Recommendation] activity name that already exists for another activity in [!DNL  Recommendations Classic], the new activity is re-synced with a new name. The new name is the original name appended with a timestamp to make it unique. This new name is displayed in both [!DNL  Target Standard/Premium] and [!DNL  Recommendations Classic]. 

>1. When finished, click ** [!UICONTROL  Save] **.

>       An overview of your activity is displayed. From the [!UICONTROL  Overview] page, you can: 

>    
>    * Activate the activity 

>    * Edit the activity 

>    * Pin the activity to your Marketing Cloud board 

>    * View your experience URLs 

>    * Download data 

>    * Change the percentage of activity entrants who see the control experience 

>    * Show or hide criteria details 

>    * View the code for your designs 


>1. (Optional) Open the [!UICONTROL  Reports] page to view the report that shows the performance of your [!DNL  Recommendations] activity.
>1. (Optional) Open the [!UICONTROL  Collisions] page to view any [ activity collisions ](https://marketing.adobe.com/resources/help/en_US/target/target/c_activity_collisions.html) that might occur.

>       Activity collisions occur when multiple activities are set to deliver content to the same page, and may cause unexpected content to be displayed. 
>## Criteria {#concept_3F1D81F2EEC64B79981D07C7BE4CC73E}Criteria are rules that determine which products to recommend based on a predetermined set of visitor behaviors. 
<draft-comment>
  New pointer topic. 
</draft-comment>Criteria determine which action will result in which recommendation. You can test multiple recommendation types against each other by adding multiple criteria. 

For more information, see [ Criteria ](c_algorithms.md#concept_4BD01DC437F543C0A13621C93A302750). 
>## Design {#concept_FEDC0CD889224A4984006307E151D94B}Designs define how recommendations appear on a page. 
<draft-comment>
  New pointer topic. 
</draft-comment>For more information, see [ Design Overview ](c_design-overview.md#concept_3A265774E088420C90983C9A8C04640A). 
>## Adding Promotions {#task_CC5BD28C364742218C1ACAF0D45E0E14}Add promoted items and control their placement in your 
<keyword>
  Recommendations 
</keyword> designs. You can add static and dynamic promotions. 
<draft-comment otherprops="merge">
  recs/t_adding_promotions.xml 
</draft-comment>
>[!IMPORTANT]
>
>Static and dynamic exclusion rules are powerful features that can help you with your marketing efforts. For detailed information, examples, and use-case scenarios, see[ Use Dynamic and Static Inclusion Rules ](t_create_recs_activity.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F). 



When you create a [!DNL  Recommendations] activity, you have the option to include promoted items in your [!DNL  Recommendations] design. Promotions use available slots in a design and take precedence over criteria results and backup recommendations. For example, if your design has six slots and you use two of them for promotions, four slots are available for items recommended based on criteria. 

You can promote specific items, dynamically promote items, promote items based on attributes, or promote collections. 

![](graphics/add_promotion_toggles.png) 


>[!NOTE]
>
>Using promotions changes CSV structure and output. These changes could have an impact on any external processes that involve CSV, such as email.



>1. On the ** [!UICONTROL  Add Promotions] ** screen, click either the ** [!UICONTROL  Front Promotion] ** or ** [!UICONTROL  Back Promotion] ** toggle.

>       ![](graphics/add_promotion_front.png) 

>       You can insert promotions both before *and* after your criteria results. 
>1. Set the number of design slots to use for promoted items.

>    [!DNL  Recommendations]1. Set a start date and end date for your promoted items.

>1. Select a ** [!UICONTROL  Promotion Type] **.

>    
>    * Select ** [!UICONTROL  List of items] ** and enter the ` entity.id` values, separated by commas, of the specific items you want to promote. 

>      If your list includes more items than the number of slots you set for promotions, you can select the ** [!UICONTROL  Randomize item order] ** check box to vary the promoted items that are displayed in your design. 

>    * Select ** [!UICONTROL  Promote by attribute] ** and add rules to define the attributes of the items you want to promote. 

>      If you select Promote by Attribute, you can create dynamic matches. For more information, see [ Use Dynamic and Static Inclusion Rules ](t_create_recs_activity.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F). 

>    * Select ** [!UICONTROL  Promote a collection] ** and choose the collection of items you want to promote. You can create new collections to use for promotions. See [ Create a Collection ](c_products.md#task_1256DFF6842141FCAADD9E1428EF7F08) for more information. 

>1. Click ** [!UICONTROL  Save.] **.

>       Promotions are applied to all experiences in the activity. 
>## Use Dynamic and Static Inclusion Rules {#concept_4CB5C0FA705D4E449BD0B37B3D987F9F}Information about creating inclusion rules for criteria and promotions, and adding additional dynamic or static filtering rules to achieve better results. 
<draft-comment otherprops="merge">
  recs/c_use-dynamic-and-static-inclusion-rules.xml 
</draft-comment>The process for creating and using inclusion rules for criteria and promotions is similar, as are the use cases and examples. Both criteria and promotions and the use of inclusion rules are covered in this topic. 

This section contains the following information: 


* [ Adding Filtering Rules to Criteria ](t_create_recs_activity.md#section_CD0D74B8D3BE4A75A78C36CF24A8C57F)
* [ Adding Filtering Rules to Promotions ](t_create_recs_activity.md#section_D59AFB62E2EE423086281CF5D18B1076)
* [ Filter Types ](t_create_recs_activity.md#section_0125F1ED10A84C0EB45325122460EBCD)
* [ Handling Empty Values when Filtering by Entity Attribute Matching, Profile Attribute Matching, and Parameter Matching ](t_create_recs_activity.md#section_7D30E04116DB47BEA6FF840A3424A4C8)
* [ Dynamic Filter Scenarios ](t_create_recs_activity.md#section_9873E2F22E094E479569D05AD5BB1D40)
* [ Caveats ](t_create_recs_activity.md#section_A889FAF794B7458CA074DEE06DD0E345)


## Adding Filtering Rules to Criteria {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

While you are [ creating criteria ](c_algorithms.md#task_8A9CB465F28D44899F69F38AD27352FE), click ** [!UICONTROL  Add Filtering Rule] ** under ** [!UICONTROL  Inclusion Rules] **. 

![](graphics/inclusion options.png) 

The available options vary depending on the selected industry vertical and recommendation key. 

## Adding Filtering Rules to Promotions {#section_D59AFB62E2EE423086281CF5D18B1076}

While [ creating a promotion ](t_create_recs_activity.md#task_CC5BD28C364742218C1ACAF0D45E0E14), select ** [!UICONTROL  Promote by Attribute] **, then click ** [!UICONTROL  Add Filtering Rule] **. 

![](graphics/inclusion options promotion.png) 

## Filter Types {#section_0125F1ED10A84C0EB45325122460EBCD}

The following table lists the types of filtering options for both criteria and promotions: 



<table id="table_605D70D1824340279387637819AD1A05"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type </th> 
   <th colname="col2" class="entry"> Option </th> 
   <th colname="col3" class="entry"> Available Operators </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="2"> <p><b>Dynamic Filtering</b> </p> </td> 
   <td colname="col2"> <p><b>Entity Attribute Matching: </b>Filter dynamically by comparing a pool of potential recommendations items to a specific item that the users has interacted with. </p> <p>For example, only recommend items that match the current item’s brand. </p> </td> 
   <td colname="col3"> <p>equals </p> <p>does not equal </p> <p>is between </p> <p>contains </p> <p>does not contain </p> <p>starts with </p> <p>ends with </p> <p>value is present </p> <p>value is not present </p> <p>is greater than or equal to </p> <p>is less than or equal to </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Profile Attribute Matching: </b>Filter dynamically by comparing items (entities) against a value in the user's profile. </p> <p>For example, only recommend items that match the visitor’s favorite brand. </p> </td> 
   <td colname="col3"> <p>equals </p> <p>does not equal </p> <p>contains </p> <p>does not contain </p> <p>starts with </p> <p>ends with </p> <p>is greater than or equal to </p> <p>is less than or equal to </p> <p>is between </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Parameter Matching: </b>Filter dynamically by comparing items (entities) against a value in the request (API or mbox). </p> <p>For example, only recommend content that matches the "industry" page parameter. </p> <p> <p type="important">Note:  If the activity was created before October 31, 2016, its delivery will fail if it uses the "Parameter Matching" filter. To work around this problem: <p> 
       <ul id="ul_0F41B82D21A940CC94A1155D19E890E0"> 
        <li id="li_CBACB09973FB4A65949E34826B7FD72C">Create a new activity and add your criteria in it. </li> 
        <li id="li_9FEF18BCB138488DAC8460764F9A143C">Use a criteria that does not contain the "Parameter Matching" filter. </li> 
        <li id="li_7A20F76AD7C44A19BB9E1516D8663C50">Remove the "Parameter Matching" filter from your criteria. </li> 
       </ul> </p> </p> </p> </td> 
   <td colname="col3"> <p>equals </p> <p>does not equal </p> <p>contains </p> <p>does not contain </p> <p>starts with </p> <p>ends with </p> <p>is greater than or equal to </p> <p>is less than or equal to </p> <p>is between </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Filter by Value</b> </p> </td> 
   <td colname="col2"> <p><b>Static Filter: </b>Manually enter one or more static values to filter. </p> <p>For example, only recommend content with an MPAA rating of "G" or "PG." </p> </td> 
   <td colname="col3"> <p>equals </p> <p>does not equal </p> <p>contains </p> <p>does not contain </p> <p>starts with </p> <p>ends with </p> <p>value is present </p> <p>value is not present </p> <p>is greater than or equal to </p> <p>is less than or equal to </p> </td> 
  </tr> 
 </tbody> 
</table>


>[!NOTE]
>
>If you are familiar with how inclusion rules were configured prior to the Target 17.6.1 release (June 2017), you'll notice that some of the options and operators have changed. Only those operators applicable to the selected option display and some operators were renamed ("matches" is now "equals") to be more consistent and intuitive. All existing exclusion rules created prior to this release were automatically migrated into the new structure. No restructuring is necessary on your part.



You can create as many inclusion rules as necessary. The inclusion rules are joined with an AND operator. All rules must be met to include an item in a recommendation. 

Dynamic criteria and promotions are much more powerful than static criteria and promotions, and yield better results and engagement. The following examples will give you ideas about how you can use dynamic promotions in your marketing efforts: 

**Equals: **Using the "equals" operator in dynamic promotions, when a visitor is viewing an item on your website (such as a product, article, or movie), you can promote other items from: 


<ul class="simplelist"> 
 <li> the same brand </li> 
 <li> the same category </li> 
 <li> the same category AND from the house brand </li> 
 <li> the same store </li> 
</ul>



**Does Not Equal: **Using the "does not equal" operator in dynamic promotions, when a visitor is viewing an item on your website (such as a product, article, or movie), you can promote other items from: 


<ul class="simplelist"> 
 <li> a different TV series </li> 
 <li> a different genre </li> 
 <li> a different product series </li> 
 <li> a different style ID </li> 
</ul>



**Is Between: **Using the "is between" operator in dynamic promotions, when a visitor is viewing an item on your website (such as a product, article, or movie), you can promote other items that are: 


<ul class="simplelist"> 
 <li> more expensive </li> 
 <li> less expensive </li> 
 <li> cost plus or minus 30% </li> 
 <li> later episodes in the same season </li> 
 <li> prior books in a series </li> 
</ul>



## Handling Empty Values when Filtering by Entity Attribute Matching, Profile Attribute Matching, and Parameter Matching {#section_7D30E04116DB47BEA6FF840A3424A4C8}

You can choose several options to handle empty values when filtering by Entity Attribute Matching, Profile Attribute Matching, and Parameter Matching for exit criteria and promotions. 

Previously, no results were returned if a value was empty. The "If *x* is Empty" drop-down list lets you choose the appropriate action to perform if the criteria has empty values, as shown in the following illustration: 

![](graphics/empty value.png) 

To select the desired action, hover over the gear icon (  ![](graphics/icon_gear.png) ), then choose the desired action: 



<table id="table_DB442803C2654F18A62517E19B4E3974"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Action </th> 
   <th colname="col02" class="entry"> Available For </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ignore this filtering rule </p> </td> 
   <td colname="col02"> <p>Profile Attribute Matching </p> <p>Parameter Matching </p> </td> 
   <td colname="col2"> <p>This is the default action for Profile Attribute Matching and Parameter Matching. </p> <p>This option specifies that the rule is ignored. For example, if there are three filtering rules and the third rule doesn't pass any values, instead of not returning any results, you can simply ignore the third rule with the empty values. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Do not show any results for this criteria </p> </td> 
   <td colname="col02"> <p>Entity Attribute Matching </p> <p>Profile Attribute Matching </p> <p>Parameter Matching </p> </td> 
   <td colname="col2"> <p>This is the default action for Entity Attribute Matching. </p> <p>This action is how Target handled empty values before the addition of this option: no results will be shown for this criteria. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Use a static value </p> </td> 
   <td colname="col02"> <p>Entity Attribute Matching </p> <p>Profile Attribute Matching </p> <p>Parameter Matching </p> </td> 
   <td colname="col2"> <p>If a value is empty, you can choose to use a static value. </p> </td> 
  </tr> 
 </tbody> 
</table>

As an example of handling empty values, consider [ Scenario 9 ](t_create_recs_activity.md#section_9873E2F22E094E479569D05AD5BB1D40) below: 

## Dynamic Filter Scenarios {#section_9873E2F22E094E479569D05AD5BB1D40}

**Scenario 1: **Instead of matching an item in a catalog to other items in a catalog using a static filter, you can use a dynamic filter to match an item in a catalog to an attribute from the visitor's profile. 

For example, you could use the [!UICONTROL  Profile Attribute Matching] option to create a rule that recommends items only where the brand equals the value or text stored in ` profile.favoritebrand`. With such a rule, if a visitor is looking at running shorts from a particular brand, only recommendations will display that match that user's favorite brand (the value stored in ` profile.favoritebrand` in the visitor's profile). 

**Scenario 2: **Before Target added the ability to use attribute information from a visitor's profile, if you were setting up job listings that would display only to job seekers from a specific location and with a specific college degree, you would have had to set up many activities with different audiences (one for each city and degree). If you have job listings in many cities, this task became burdensome. 

You can now use inclusion rules to match a job seeker's location and degree from his or her visitor's profile to a job listing, as shown in the following example: 

![](graphics/job seeker.png) 

The job listing on the left side requires that the visitor is in San Francisco, New York, or Los Angeles ( ` entity.jobCity`) and have either a BSCS or MBA degree ( ` entity.requiredDegree`). 

This job seeker on the right side is in Los Angeles ( ` profile.usersCity`) and has an MBA degree ( ` profile.degree`). 

Using a dynamic filter with profile attribute matching, you can create the filter displayed in the lower portion of the above illustration that will recommend only job listings that this visitor qualifies for based on location and degree. 

The criteria for these filters are as follows: 

```
entity.jobCity&amp;nbsp;-&amp;nbsp;equals&amp;nbsp;-&amp;nbsp;the&amp;nbsp;value/text&amp;nbsp;stored&amp;nbsp;in&amp;nbsp;-&amp;nbsp;profile.usersCity
```
and 

```
entity.requiredDegree&amp;nbsp;-&amp;nbsp;equals&amp;nbsp;-&amp;nbsp;the&amp;nbsp;value/text&amp;nbsp;stored&amp;nbsp;in&amp;nbsp;-&amp;nbsp;profile.degree
```
Dynamic filters using profile attribute matching allows you to do more with fewer activities, as shown below: 

![](graphics/dynamic before and after.png) 

The diagram in the top of the above illustration depicts how dynamic filters using profile attributes work. You can create one audience that uses criteria (in the above scenario, city and degree) to display a job listing that the visitor qualifies for. This filter works for an almost infinite number of possibilities regarding location and degree. 

The diagrams in the bottom of the illustration depicts just two of the many audiences that you would have had to set up if you are not configuring a criteria or promotion with dynamic filters using profile attributes. You would have to set up a different audience for each city and for each degree. The number of needed audiences could quickly become unmanageable, especially if you had a large number of job listings in various cities. 

Without using profile attributes, your audiences and experiences would look like the top half of the following illustration, but with additional audience/experience pairs for every conceivable scenario. 

![](graphics/dynamic audience experience pairs.png) 

Dynamic filters using profile attributes that match entity attributes to user attributes let you set up one audience that dynamically, on the fly, delivers the desired experience, as shown in the bottom half of the above illustration. 

As long as you have the required information embedded into each job listing and you are capturing the required information within the user profiles, creating and managing audiences and experiences is greatly simplified. 

**Scenario 3: ** A sports company wants to show articles on its website for teams that a person cares about. Every article could have a field with ` entity.featuredTeams` that includes all teams discussed in the article. Every profile attribute could have a list of favorite teams the user is "subscribing" to. 

A sample inclusion rule would could look like the following: 

Include only when ` entity.featuredTeam` has one or more values that match ` profile.favoriteTeams`. 

When considering the following examples, remember that at least one entire string value needs to match (completely). There is no match if none of the strings match. Note the de-coupling of the entity attributes in the matching rules. This allows for matching between different metadata fields. 



<table id="table_E5EB0F6494804183B358E5F17D0B4BCC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Examples/Descriptions </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
      "entity.featuredTeam"&amp;nbsp;-&amp;nbsp;"Athletics,Red&amp;nbsp;Sox"&amp;nbsp;equals&amp;nbsp;"profile.favoriteTeams"&amp;nbsp;-&amp;nbsp;"Athletics" 
    </codeblock> <p>Considered a match because "Athletics" equals, even though "Red Sox" does not. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
      "entity.featuredTeam"&amp;nbsp;-&amp;nbsp;"Athletics,Red&amp;nbsp;Sox"&amp;nbsp;equals&amp;nbsp;"profile.favoriteTeams"&amp;nbsp;-&amp;nbsp;"Athletics,Red&amp;nbsp;Sox" 
    </codeblock> <p>Considered a match because both "Athletics" and "Red Sox" equals, although it is not necessary for both teams to match. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
      "entity.featuredTeam"&amp;nbsp;-&amp;nbsp;"Athletics"&amp;nbsp;equals&amp;nbsp;"profile.favoriteTeams"&amp;nbsp;-&amp;nbsp;"Athletics,Red&amp;nbsp;Sox" 
    </codeblock> <p>Considered a match because "Athletics" equals, even though "Red Sox" does not. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
      "entity.featuredTeam"&amp;nbsp;-&amp;nbsp;"Athletics"&amp;nbsp;equals&amp;nbsp;"profile.favoriteTeams"&amp;nbsp;-&amp;nbsp;"Athletic" 
    </codeblock> <p>Does not match because "Athletics" (plural) does not equal "Athletic" (singular). </p> <p>Alternatively, you could use "contains" instead of "equals" to make this a match. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
      "entity.featuredTeam"&amp;nbsp;-&amp;nbsp;"Athletic"&amp;nbsp;equals&amp;nbsp;"profile.favoriteTeams"&amp;nbsp;-&amp;nbsp;"Athletics" 
    </codeblock> <p>Does not match because "Athletic" (singular) does not equal "Athletics" (plural). </p> <p>Alternatively, you could use "starts with" instead of "equals" to make this a match. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Scenario 4: **The following illustration demonstrates how to use the "equals" and "is between" operators to promote more expensive items that are from the same category and the same brand. For example, a sporting apparel company can promote more expensive running shoes in an effort to up-sell a visitor looking at running shorts. 

![](graphics/dynamic3.png) 

The following rules are used in this example: 

```
category - equals - current item's - category 
And 
brand - equals - current item's - brand 
And 
value - is between - 100% and 1000% of - current item's - value
```

>[!NOTE]
>
>You cannot change the key in a dynamic promotion with multiple rules (the third drop-down list in the first two rules labeled "Current Item's" in the illustration).



**Scenario 5: **The second illustration demonstrates how to use the "equals" and "is between" operators to promote more expensive items that are from the same category, the same brand, and the house brand. For example, an office supply company can promote more expensive toner cartridges, of both the same brand and the company's house brand, in an effort to up-sell a visitor looking at printers. 

![](graphics/dynamic4.png) 

The following rules are used in this example: 

```
category - equals - current item's - category 
And 
IsHouseBrand - equals - true 
And 
value - is between - 100% and 1000% of - current item's - value
```
Notice that this example uses two dynamic rules and one static rule. 

**Scenario 6: **The third illustration demonstrates how to use the"does not equal" operator to promote a series that does not equal the series that the visitor is currently viewing. For example, a media website could promote a television series that is different than the series the visitor is currently viewing. 

![](graphics/dynamic5.png) 

The following rule is used in this example: 

```
series&amp;nbsp;-&amp;nbsp;does&amp;nbsp;not&amp;nbsp;equal&amp;nbsp;-&amp;nbsp;current&amp;nbsp;item's&amp;nbsp;-&amp;nbsp;series
```
**Scenario 7: **The fourth illustration demonstrates how to promote compatible accessory items for the visitor's last-purchased item. For example, if someone purchased a new TV, you could dynamically promote an HDMI cable. 

![](graphics/dynamic1.png) 

The following rules are used in this example: 

```
id&amp;nbsp;-&amp;nbsp;equals&amp;nbsp;-&amp;nbsp;last&amp;nbsp;purchased&amp;nbsp;item's&amp;nbsp;-&amp;nbsp;compatibleAccessoryids
```
**Scenario 8: **The next illustration demonstrates how to promote items that are on sale for between 90 and 110 percent of the item the visitor is currently viewing. For example, if someone is looking at a TV, you could dynamically promote similar TVs that are on sale in approximately the same price range. 

![](graphics/dynamic2.png) 

The following rules are used in this example: 

```
salesPrice&amp;nbsp;-&amp;nbsp;is&amp;nbsp;between&amp;nbsp;-&amp;nbsp;90%&amp;nbsp;and&amp;nbsp;110%&amp;nbsp;of&amp;nbsp;-&amp;nbsp;current&amp;nbsp;item's&amp;nbsp;-&amp;nbsp;price
```
**Scenario 9: **Consider the following scenario for a sport's media site about how to handle empty values, as explained in [ Handling Empty Values when Filtering by Entity Attribute Matching, Profile Attribute Matching, and Parameter Matching ](t_create_recs_activity.md#section_7D30E04116DB47BEA6FF840A3424A4C8) above: 

The content team for a sport's media site wants to show content to users for their favorite teams. If a user has specified a favorite team, the team wants to show media for that team. If a user has not specified a favorite team, the team can use the "If *x* is Empty" drop-down list to do one of the following: 


* Use the [!UICONTROL  Ignore This Filtering Rule] option to ignore the team filter altogether, as shown in the following illustration: 

  ![](graphics/missing1.png) 

* Use the [!UICONTROL  Do Not Show Any Results for This Criteria] option to not show any media as part of this criteria, as shown in the following illustration: 

  ![](graphics/missing7.png) 

* Use the [!UICONTROL  Use a Static Value] option to show media for a specific team (49ers, for example), as in the following illustration: 

  ![](graphics/missing10.png) 



## Caveats {#section_A889FAF794B7458CA074DEE06DD0E345}


>[!IMPORTANT]
>
>Different data type attributes might not be compatible in dynamic criteria or promotions during runtime with the "equals" and "does not equal" operators. You should use Value, Margin, Inventory, and Environment values wisely on the right hand side if the left hand side has predefined attributes or custom attributes.



![](graphics/left_right.png) 

The following table shows effective rules and rules that might not be compatible during runtime: 



<table id="table_CDDDC41C55EA4D23A910CC0747F31435"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Compatible Rules </th> 
   <th colname="col2" class="entry"> Potential Incompatible Rules </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value - is between - 90% and 110% of current item's - salesValue </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> salesValue - is between - 90% and 110% of current item's - value </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value - is between - 90% and 110% of current item's - value </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> clearancePrice - is between - 90% and 110% of current item's - margin </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin - is between - 90% and 110% of current item's - margin </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> storeInventory - equals - current item's - inventory </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inventory - equals - current item's - inventory </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
 </tbody> 
</table>

>## Recommendations Activity Settings {#reference_3FDA8388CEEC4159949151C1829E2FBB}Several settings can be used to describe and control a 
<keyword>
  Recommendations 
</keyword> activity. 
<draft-comment otherprops="merge">
  recs/r_recs_activity_settings.xml 
</draft-comment>
>This video includes information about activity settings. 

><table id="table_A3A70CC0C9F54131BB9F098B4DA8C9D6"> 
 <thead> 
  <tr> 
   <th class="entry" colspan="2"> Activity Settings </th> 
   <th colname="col3" class="entry"> 3:02 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colspan="2"> 
    <div class="video-iframe"> 
     <iframe src="https://www.youtube.com/embed/6XNEM8tUADo/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://www.youtube.com/embed/6XNEM8tUADo/</iframe>
    </div> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_FF4FEC7BC7A34461BAA54FBE18A8E63B"> 
      <li id="li_7D6D4CB2E771430F84D2B658F8611532">Enter an objective for your activity </li> 
      <li id="li_61D9DDCD3AFB40E2BC55AFED5CD6C405">Set the priority level of your activities </li> 
      <li id="li_745F20CC95DF4BE48173991CB42EC50A">Schedule activity start and end times </li> 
      <li id="li_699D4D5D089A4FB7BA4C5E95337AC34A">Add audiences for reporting to create report filters </li> 
      <li id="li_0EDDBA5E70B54F22A76F1D6D722914BE">Enter notes for your activities </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

>The following table describes the available settings for a Recommendations activity. 

><table id="table_E6006EA8C4B94DB5A03CD5DB971F5178"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Setting </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Name </td> 
   <td colname="col2"> <p>Provide a descriptive name that will help you and your team identify the activity. </p> <p>The following characters are not allowed in an activity name: </p> <p> 
     <ul id="ul_019C0E7C8B9945CA9EF7A0721F506800"> 
      <li id="li_6A7CA8BB78E64A8DA8573D8FAAF896EB">/ </li> 
      <li id="li_6406D6FE934D4E7BB7791BEED3A209F2">? </li> 
      <li id="li_6D6B3DEEF00F4AC2A9F4915FF0D8AC64"># </li> 
      <li id="li_CDB071C41D2E45BAB431679D9B735266">: </li> 
     </ul> </p> <p>If you specify a <span class="keyword"> Recommendations </span> activity name that already exists for another activity in <span class="keyword"> Recommendations Classic </span>, the new activity is resynced with a new name. The new name is the original name appended with a timestamp to make it unique. This new name is displayed in both <span class="keyword"> Target Standard/Premium </span> and <span class="keyword"> Recommendations Classic </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Objective </td> 
   <td colname="col2"> <p>(Optional) Describe the goal of the activity. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Priority </td> 
   <td colname="col2"> <p>Adjust the slider to determine the priority level. There are three levels: </p> <p> 
     <ul id="ul_FCA07A04D6F248759429BC46BA57CCE5"> 
      <li id="li_88F440506D22467295C71F2B14470AD7">0 = Low </li> 
      <li id="li_AEC7893759464944A6501FA742A2B0FE">1 = Medium </li> 
      <li id="li_B329FB669546477DBDA27E51369D1878">2 = High </li> 
     </ul> </p> <p>The priority is used if multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority displays. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Duration </td> 
   <td colname="col2"> <p>Set the duration of the activity. </p> <p>The activity can start when approved, or you can set a specific date and time. Likewise, the activity can either end when it is deactivated or you can set a date and time. The time picker uses a 24-hour clock, with 00:00 being midnight. The time zone is set to the time zone configured in your browser. To use a different time zone, set your browser to another time zone and restart the browser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Reporting Settings </td> 
   <td colname="col2"> 
    <ul id="ul_74509C88F0024849AC36AF6125780CF2"> 
     <li id="li_15A4260BCE114E3683FED75CD11B7D6F"> <p><b>Goal: </b>Name the goal, and select the success metric that determines whether the activity is successful. </p> </li> 
     <li id="li_62C0B5A4D5CE40BDB9FFF6D452B70A72"> <p><b>Additional Metrics: </b>Configure additional success metrics to be used in your reports. </p> </li> 
     <li id="li_1AD0F3946E1348429F77A52CDD1FBB4D"> <p><b>Audiences for Reporting: </b>Define audiences that can be used when filtering your reports. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Other Metadata </td> 
   <td colname="col2"> <p>Enter notes about your activity. </p> </td> 
  </tr> 
 </tbody> 
</table>

