---
description: Insert parameter value pairs directly into the mboxCreate function. In-mbox attributes have the profile tag inserted before the attribute names.
seo-description: Insert parameter value pairs directly into the mboxCreate function. In-mbox attributes have the profile tag inserted before the attribute names.
seo-title: In-Mbox Profile Attributes
solution: Target
title: In-Mbox Profile Attributes
topic: Standard
uuid: 6331bbdb-d272-4135-afe9-562f2a24f78e
index: y
internal: n
snippet: y
translate: y
---

# In-Mbox Profile Attributes


>[!NOTE]
>
>All mbox calls, including offline calls, are limited to 50 profile values.



Click ` Audiences` > ` Profile Scripts`, then type the in-mbox attribute to search for. 


```
<script type="text/javascript"> 
 
mboxCreate('mboxTitle','profile.PARAMETER1=VALUE1','profile.PARAMETER2=VALUE2','profile.PARAMETER3=VALUE3'); 
 
</script>
```



>[!NOTE]
>
>Attribute names cannot contain spaces.


