---
description: This topic shows how to create a carousel that can be edited in the Visual Experience Composer (VEC).
keywords: Visual Experience Composer;VEC;carousel
seo-description: This topic shows how to create a carousel that can be edited in the Visual Experience Composer (VEC).
seo-title: Creating Carousels that Work in the Visual Experience Composer
solution: Target
subtopic: Multivariate Test
title: Creating Carousels that Work in the Visual Experience Composer
topic: Standard
uuid: d5d4bc83-1c14-49f7-919d-6caaccbdaa43
index: y
internal: n
snippet: y
translate: y
---

# Creating Carousels that Work in the Visual Experience Composer

When you use the steps below, [!DNL  Target] always knows that the selected slide will have the 'selector' for the correct slide, even if it is changed in the Visual Experience Composer after a few seconds. 

>1. Create static HTML placeholders.

>    
>       ```
>       <ul>
>       <li class="show"> slide 1 </li>
>       <li class="hidden"> slide 2 </li>
>       <li class="hidden"> slide 3 </li>
>       </ul>
>       ```

>1. Add CSS to design the look and feel.

>       Don't use JavaScript for this. 


>       >[!NOTE]
>       >
>       >The [!UICONTROL  Render Using JavaScript] option is currently not supported if it is used along with custom code in the Visual Experience Composer. 

>1. Only update the classNames to hide others and show the next with timer/animation.

