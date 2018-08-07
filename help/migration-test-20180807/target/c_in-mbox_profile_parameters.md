---
description: Insert parameter value pairs directly into the mboxCreate function. In-mbox attributes have the profile tag inserted before the attribute names.
seo-description: Insert parameter value pairs directly into the mboxCreate function. In-mbox attributes have the profile tag inserted before the attribute names.
seo-title: In-Mbox Profile Attributes
solution: Target
title: In-Mbox Profile Attributes
topic: Standard
uuid: 8ab14680-a284-45b8-ae66-b43f459a098c
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


To associate In-Mbox Profile Attributes with an Mbox:

1. Inserting an mbox.

1. After the mbox title, enter the in-mbox profile attributes and values you wish to add to the mbox.
   Parameters and values are case sensitive. Match the case of the parameters and values you will receive during the campaign or test.


