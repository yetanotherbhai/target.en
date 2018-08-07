---
description: Automated Personalization collects a variety of data.
seo-description: Automated Personalization collects a variety of data.
seo-title: Automated Personalization Data Collection
solution: Target
title: Automated Personalization Data Collection
topic: Premium
uuid: b334c742-a337-4888-9575-702d1be3b5b8
index: y
internal: n
snippet: y
translate: y
---

# Automated Personalization Data Collection


>The following table shows the data collected by Automated Personalization by default, without the marketer having to do anything. You can augment the input data set at any time.


><table id="table_F46105983FD14051BBE9C429EE9B2ACB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry">Data Type</th> 
   <th colname="col2" class="entry">Details</th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">Shared Audiences</td> 
   <td colname="col2"> <p>Created through:</p> <p> 
     <ul id="ul_FFC96DB0C89A4563B83B8BFACA57A766"> 
      <li id="li_1A6F8C26F6EB48DAA6FAD9ED106A671E">Adobe Audience Manager</li> 
      <li id="li_B31BAFFAB5BA4B4F9C05BF6F5467802B">Adobe Target Classic</li> 
      <li id="li_1009D43E727246ABA61CF66A80C744EF">Adobe Analytics</li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">URL Parameters</td> 
   <td colname="col2">Anything present in the URLs</td> 
  </tr> 
  <tr> 
   <td colname="col1">Interest Areas</td> 
   <td colname="col2"> <p>Automated Personalization uses crawler technology that develops key tokens characterizing content within each page URL. The technique used is generally known as term-frequency/inverse-document-frequency or TF/IDF. These tokens are then stored in each user profile as the user crawls through different pages. These tokens are recency ranked. For example:</p> <p> 
     <table id="table_366C8BDF8D294BC0B24B579D96A35B2E">  
     </table> </p> <p>If a visitor views url1 and then url4, then the user profile, that visitor will have following ordered interest areas:</p> <p> 
     <ol id="ol_DB8451DEA9314251B827AF91ACB81573"> 
      <li id="li_D77E3351C9944F9E83A9A15C90D31C2E">black</li> 
      <li id="li_B279553BDB054642B3F8EE18362B79A1">coat</li> 
      <li id="li_538103CC3C8246B59DCC142BFFF5D55F">rain</li> 
      <li id="li_8026751986194534BEAD0D3030B27202">shoe</li> 
      <li id="li_3F586ACBC2F344DAB41A86915B7EE43E">heel</li> 
     </ol> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">User Profile Parameters</td> 
   <td colname="col2">Information stored in the user profile</td> 
  </tr> 
  <tr> 
   <td colname="col1">Mbox Parameters</td> 
   <td colname="col2"> <p> 
     <ul id="ul_7F3F3C41B9D148748503FBC9B4FE203D"> 
      <li id="li_9EB369DDE3814B2BBBD24BB0ACEB1A57"> <span class="codeph">BOX_mboxTime</span> </li> 
      <li id="li_E07C25901FAC4A6785CDACF48849009A"> <span class="codeph">BOX_mboxXDomain</span> </li> 
      <li id="li_F6E4DA11D3C743B78FF99EB23E9494B9"> <span class="codeph">BOX_mboxXDomainCheck</span> </li> 
      <li id="li_9567463BCF984AE9A44403D50F1EE7BC">Other information passed by mboxes</li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Environment/Technographics</td> 
   <td colname="col2"> <p> 
     <ul id="ul_9C5FCB33757B49B7986C1C8FADCF479C"> 
      <li id="li_5CC0454891494C58BEDF152A3121E417"> <span class="codeph">ENV_Browser</span> </li> 
      <li id="li_0BE7968D9E2D4C08839500B7373B14AA"> <span class="codeph">ENV_BrowserHeight</span> </li> 
      <li id="li_6093F549D55D4540AE621ADD915A687F"> <span class="codeph">ENV_BrowserTimezoneOffsetMinutes</span> </li> 
      <li id="li_2944DD932D95464988AEC74DD86A0F7B"> <span class="codeph">ENV_BrowserVersion</span> </li> 
      <li id="li_96AADEAD6A494845B58E9E2EE595DCFD"> <span class="codeph">ENV_BrowserWidth</span> </li> 
      <li id="li_38DE5712CE0447C982B4092B54E7F32C"> <span class="codeph">ENV_ColorDepth</span> </li> 
      <li id="li_CDFDA212FEDD43C392E7D0D488EB2DF4"> <span class="codeph">ENV_DayOfWeek</span> </li> 
      <li id="li_B13473B801BC4AC4B8B60CAAD52E6167"> <span class="codeph">ENV_Language</span> </li> 
      <li id="li_C598D22AF2E947F7AB89F6862BA8BF4E"> <span class="codeph">ENV_LocalTimePeriod</span> </li> 
      <li id="li_BD9850B487CD4C9E978E16D938F3385C"> <span class="codeph">ENV_OperatingSystem</span> </li> 
      <li id="li_F6345E117AAE462A87F0C3ED2390F13B"> <span class="codeph">ENV_OperatingSystemVersion</span> </li> 
      <li id="li_995338C827F34CB2B274C12B601CF386"> <span class="codeph">ENV_PageId</span> </li> 
      <li id="li_71A320C5E84C4C7B96D425FEE6FD4B2B"> <span class="codeph">ENV_Referrer</span> </li> 
      <li id="li_3B39DA2B08F14CAEA4F177CF022F3E5B"> <span class="codeph">ENV_ScreenHeight</span> </li> 
      <li id="li_E8EAD35B4D65496A8A949EDA4AD09CE1"> <span class="codeph">ENV_ScreenWidth</span> </li> 
      <li id="li_2587338069C2465E93D5AB3C22A7C9DD"> <span class="codeph">ENV_ServerHour</span> </li> 
      <li id="li_8005A679EB43456BABE32B4D3AE8F644"> <span class="codeph">ENV_UserHour</span> </li> 
      <li id="li_8F151294CD6C414A8EC5D5BFBF93429C"> <span class="codeph">ENV_UserHourType</span> </li> 
      <li id="li_56B58005720C4A31876DB6C0D57D6F62"> <span class="codeph">ENV_WeekHour</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geography</p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_1A91E143076C4970A3BF0DF15649555D"> 
      <li id="li_63A72EC470594ED2905C5368D6598536"> <span class="codeph">GEO_City</span> </li> 
      <li id="li_2369DE40B88D4032976D3E2D35CC49DD"> <span class="codeph">GEO_Country</span> </li> 
      <li id="li_5A3ABFF39CED451D866654E46E46CAC2"> <span class="codeph">GEO_DMA</span> </li> 
      <li id="li_0DFB24429C354A2A83D526F51C3F25DC"> <span class="codeph">GEO_Latitude</span> </li> 
      <li id="li_BCA9361B01914CFE85EFF4E36F5AD431"> <span class="codeph">GEO_Longitude</span> </li> 
      <li id="li_1849BB1B82F74D22807DB97BBAD9A937"> <span class="codeph">GEO_Region</span> </li> 
      <li id="li_46B4BDEE6E9041EBB5FF24E08B9145E1"> <span class="codeph">GEO_ZipCode</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Device</p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6E22B6B5C0A84E7EBA1A5EF436FF62EC"> 
      <li id="li_677A553C77E747438B9792649024697E"> <span class="codeph">MOB_targeting.mobile.model</span> </li> 
      <li id="li_2F49F9701DB34A69AFE4B70380818401"> <span class="codeph">MOB_targeting.mobile.vendor</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>User Session</p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_41AB5DEA936C43959AC1F1A6A179C3F5"> 
      <li id="li_F25F9BE374144A00B42632179FCDE1F8"> <span class="codeph">SES_CUMULATIVE_ACTION_1_99858</span> </li> 
      <li id="li_0862A3B8A48549AFBDB91159B427BCA1"> <span class="codeph">SES_CUMULATIVE_ORDER_VALUE</span> </li> 
      <li id="li_1BA949A060E74E99B194EC4EA76BC29A"> <span class="codeph">SES_CUMULATIVE_SUCCESSES</span> </li> 
      <li id="li_3A5CD3ED97344B29B8C7D33DC6CB089A"> <span class="codeph">SES_HOURS_SINCE_LAST_VISIT</span> </li> 
      <li id="li_D511B116BBD645A8AAB8C77DE0BC2DB0"> <span class="codeph">SES_LAST_SESSION_START</span> </li> 
      <li id="li_97F7C53DB8C04FC8B909FAFF03157726"> <span class="codeph">SES_PREVIOUS_VISIT_COUNT</span> </li> 
      <li id="li_5D0FACA15D5D494BB0801EDC5F6DBFA7"> <span class="codeph">SES_PROFILE_CREATION_TIME</span> </li> 
      <li id="li_0CB6245A3F7B468CB3A697D120C9EF90"> <span class="codeph">SES_PROFILE_UPDATE_TIME</span> </li> 
      <li id="li_DAF9A2C361B343839BD8B9A4B20132A2"> <span class="codeph">SES_RECENCY</span> </li> 
      <li id="li_15076BFF7FD54797AA86E77E8BD57388"> <span class="codeph">SES_REQEUSTS_PER_SESSION</span> </li> 
      <li id="li_B6D00FFCDA7648FDA7194079EA044FDD"> <span class="codeph">SES_SESSION_POSITION</span> </li> 
      <li id="li_6F3D04D1C99F47888000E7B3A7A6CE69"> <span class="codeph">SES_SESSION_START</span> </li> 
      <li id="li_A6618515B46C47AC8CBB07DE72DE2CFB"> <span class="codeph">SES_SESSION_TIME</span> </li> 
      <li id="li_C486DA86E8B64206B3EEE3E87C2C0ED1"> <span class="codeph">SES_SUCCESS_RECENCY</span> </li> 
      <li id="li_714839EEC68D41D5A3A1DD43C51A513B"> <span class="codeph">SES_TIME_PER_SESSION</span> </li> 
      <li id="li_9DDAAE8EAC314133BD2355427A19EDCF"> <span class="codeph">SES_TOTAL_PAGE_VIEWS</span> </li> 
      <li id="li_1D0850183CE7434E85128E0B18D37976"> <span class="codeph">SES_TOTAL_SESSIONS</span> </li> 
      <li id="li_293DBDC1D6CA4804898811E2BDE8030E"> <span class="codeph">SES_TOTAL_TIME</span> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

