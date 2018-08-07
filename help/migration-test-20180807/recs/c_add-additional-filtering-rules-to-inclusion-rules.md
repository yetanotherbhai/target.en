---
description: While creating inclusion rules for criteria or promotions, you can add additional dynamic or static filtering rules to achieve better results.
keywords: inclusion rules;inclusion criteria;recommendations;create new criteria;promotion;promotions;dynamic filtering;dynamic;filter by value;entity attribute matching;profile attribute matching;parameter matching;filter by value;static filter
seo-description: While creating inclusion rules for criteria or promotions, you can add additional dynamic or static filtering rules to achieve better results.
seo-title: Use Dynamic and Static Filters
solution: Target
title: Use Dynamic and Static Filters
topic: Premium
uuid: 7be95f29-87fc-4d06-b68f-c57df3777e33
index: y
internal: n
snippet: y
translate: y
---

# Use Dynamic and Static Filters

This section contains the following information:

* [Using Dynamic and Static Filters](c_add-additional-filtering-rules-to-inclusion-rules.md#section_A39B61E994E64FD58AEADCE022126890)
* [Dynamic Filter Use-Cases](c_add-additional-filtering-rules-to-inclusion-rules.md#section_9873E2F22E094E479569D05AD5BB1D40)


## Adding Filtering Rules {#section_A39B61E994E64FD58AEADCE022126890}

You can add additional filtering rules to criteria and promotions.
**Criteria:**While you are creating criteria, click ** `Add Filtering Rule` ** under ** `Inclusion Rules` **. 
![](graphics/inclusion options.png) 
The available options vary depending on the selected industry vertical and recommendation key.
**Promotions:**While creating a promotion, select ** `Promote by Attribute` **, then click ** `Add Filtering Rule` **. 
![](graphics/inclusion options promotion.png) 

>[!NOTE]
>
>Detailed information about dynamic promotions and inclusion rules can be found in[Add Dynamic Promotions](c_add-dynamic-matches.md#concept_2F6B81C8B7154364ACB3D6844F7573A7). 


The following table lists the types of filtering options and the available operators for each option:


<table id="table_605D70D1824340279387637819AD1A05"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Type</th> 
   <th colname="col2" class="entry">Option</th> 
   <th colname="col3" class="entry">Available Operators</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="2"> <p><b>Dynamic Filtering</b> </p> </td> 
   <td colname="col2"> <p><b>Entity Attribute Matching:</b>Filter dynamically by comparing a pool of potential recommendations items and a specific item that the users has interacted with. </p> <p>For example, only recommend items that match the current item’s brand.</p> </td> 
   <td colname="col3"> <p>equals</p> <p>does not equal</p> <p>is between</p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Profile Attribute Matching:</b>Filter dynamically by comparing items (entities) against a value in the user's profile. </p> <p>For example, only recommend items that match the visitor’s favorite brand.</p> </td> 
   <td colname="col3"> <p>equals</p> <p>does not equal</p> <p>contains</p> <p>does not contain</p> <p>starts with</p> <p>ends with</p> <p>is greater than or equal to</p> <p>is less than or equal to</p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><b>Parameter Matching:</b>Filter dynamically by comparing items (entities) against a value in the request (API or mbox). </p> <p>For example, only recommend content that matches the "industry" page parameter.</p> </td> 
   <td colname="col3"> <p>equals</p> <p>does not equal</p> <p>contains</p> <p>does not contain</p> <p>starts with</p> <p>ends with</p> <p>is greater than or equal to</p> <p>is less than or equal to</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Filter by Value</b> </p> </td> 
   <td colname="col2"> <p><b>Static Filter:</b>Manually enter one or more static values to filter. </p> <p>For example, only recommend content with an MPAA rating of "G" or "PG."</p> </td> 
   <td colname="col3"> <p>equals</p> <p>does not equal</p> <p>contains</p> <p>does not contain</p> <p>starts with</p> <p>ends with</p> <p>is greater than or equal to</p> <p>is less than or equal to</p> </td> 
  </tr> 
 </tbody> 
</table>


>[!NOTE]
>
>If you are familiar with how inclusion rules were configured prior to the Target 17.6.1 release (June 2017), you'll notice that some of the options and operators have changed. Only those operators applicable to the selected option display and some operators were renamed ("matches" is now "equals") to be more consistent and intuitive. All existing exclusion rules created prior to this release were automatically migrated into the new structure. No restructuring is necessary on your part.


You can create as many inclusion rules as necessary. The inclusion rules are joined with an AND operator. All rules must be met to include an item in a recommendation.

## Dynamic Filter Use-Cases {#section_9873E2F22E094E479569D05AD5BB1D40}

**Use-Case 1 (Favorite Brand):**Instead of matching an item in a catalog to other items in a catalog using a static filter, you can use a dynamic filter to match an item in a catalog to an attribute from the visitor's profile. 
For example, you could use the `Profile Attribute Matching` option to create a rule that recommends items only where the brand equals the value or text stored in `profile.favoritebrand`. With such a rule, if a visitor is looking at running shorts from a particular brand, only recommendations will display that match that user's favorite brand (the value stored in `profile.favoritebrand` in the visitor's profile). 
**Use-Case 2: (Job Seeker):**Before Target added the ability to use attribute information from a visitor's profile, if you were setting up job listings that would display only to job seekers from a specific location and with a specific college degree, you would have had to set up many activities with different audiences (one for each city and degree). If you have job listings in many cities, this task became burdensome. 
You can now use inclusion rules to match a job seeker's location and degree from his or her visitor's profile to a job listing, as shown in the following example:
![](graphics/job seeker.png) 
The job listing on the left side requires that the visitor is in San Francisco, New York, or Los Angeles ( `entity.jobCity`) and have either a BSCS or MBA degree ( `entity.requiredDegree`). 
This job seeker on the right side is in Los Angeles ( `profile.usersCity`) and has an MBA degree ( `profile.degree`). 
Using a dynamic filter with profile attribute matching, you can create the filter displayed in the lower portion of the above illustration that will recommend only job listings that this visitor qualifies for based on location and degree.
The criteria for these filters are as follows:

```
entity.jobCity - equals - the value/text stored in - profile.usersCity
```
and

```
entity.requiredDegree - equals - the value/text stored in - profile.degree
```
Dynamic filters using profile attribute matching allows you to do more with fewer activities, as shown below:
![](graphics/dynamic before and after.png) 
The diagram in the top of the above illustration depicts how dynamic filters using profile attributes work. You can create one audience that uses criteria (in the above scenario, city and degree) to display a job listing that the visitor qualifies for. This filter works for an almost infinite number of possibilities regarding location and degree.
The diagrams in the bottom of the illustration depicts just two of the many audiences that you would have had to set up if you are not configuring a criteria or promotion with dynamic filters using profile attributes. You would have to set up a different audience for each city and for each degree. The number of needed audiences could quickly become unmanageable, especially if you had a large number of job listings in various cities.
Without using profile attributes, your audiences and experiences would look like the top half of the following illustration, but with additional audience/experience pairs for every conceivable scenario.
![](graphics/dynamic audience experience pairs.png) 
Dynamic filters using profile attributes that match entity attributes to user attributes let you set up one audience that dynamically, on the fly, delivers the desired experience, as shown in the bottom half of the above illustration.
As long as you have the required information embedded into each job listing and you are capturing the required information within the user profiles, creating and managing audiences and experiences is greatly simplified.
**Scenario 3 (Favorite Team):** A sports company wants to show articles on its website for teams that a person cares about. Every article could have a field with `entity.featuredTeams` that includes all teams discussed in the article. Every profile attribute could have a list of favorite teams the user is "subscribing" to. 
A sample inclusion rule would could look like the following:
Include only when `entity.featuredTeam` has one or more values that match `profile.favoriteTeams`. 
When considering the following examples, remember that at least one entire string value needs to match (completely). There is no match if none of the strings match. Note the de-coupling of the entity attributes in the matching rules. This allows for matching between different metadata fields.


<table id="table_E5EB0F6494804183B358E5F17D0B4BCC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Examples/Descriptions</th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
     "entity.featuredTeam" - "Athletics,Red Sox" equals "profile.favoriteTeams" - "Athletics"
    </codeblock> <p>Considered a match because "Athletics" equals, even though "Red Sox" does not.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
     "entity.featuredTeam" - "Athletics,Red Sox" equals "profile.favoriteTeams" - "Athletics,Red Sox"
    </codeblock> <p>Considered a match because both "Athletics" and "Red Sox" equals, although it is not necessary for both teams to match.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
     "entity.featuredTeam" - "Athletics" equals "profile.favoriteTeams" - "Athletics,Red Sox"
    </codeblock> <p>Considered a match because "Athletics" equals, even though "Red Sox" does not.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
     "entity.featuredTeam" - "Athletics" equals "profile.favoriteTeams" - "Athletic"
    </codeblock> <p>Does not match because "Athletics" (plural) does not equal "Athletic" (singular).</p> <p>Alternatively, you could use "contains" instead of "equals" to make this a match.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <codeblock>
     "entity.featuredTeam" - "Athletic" equals "profile.favoriteTeams" - "Athletics"
    </codeblock> <p>Does not match because "Athletic" (singular) does not equal "Athletics" (plural).</p> <p>Alternatively, you could use "starts with" instead of "equals" to make this a match.</p> </td> 
  </tr> 
 </tbody> 
</table>

