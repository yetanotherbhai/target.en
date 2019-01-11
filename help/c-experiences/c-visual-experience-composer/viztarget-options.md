---
description: When you click on a page element, a menu shows the options that are available for that element type.
keywords: visual experience composer options;experience composer options;experience options;edit text;edit html;edit text/html;edit background color;background color;insert element;edit link;link;visual experience composer link;edit css class;css class;swap offer;offer swap;swap image;image swap;remove item;item remove;hide item;item hide;rearrange;move element;element move;resize element;element resize;element;expand selection;navigate to this link;navigate link;link navigate;navigate;link;undo;redo;undo/redo
seo-description: When you click on a page element, a menu shows the options that are available for that element type.
seo-title: Visual Experience Composer Options
solution: Target
title: Visual Experience Composer Options
topic: Standard
uuid: efd672ae-c684-455f-8ec1-0efcfe1e9534
---

# Visual Experience Composer Options{#visual-experience-composer-options}

When you click on a page element, a menu shows the options that are available for that element type.

The various VEC actions are grouped under the following Menu options to make your job quicker and more efficient:

>[!NOTE]
>
>The available options depend on the activity type you are editing.

| Menu Item | Option | Description |
|--- |--- |--- |
|Edit|Text/HTML|Change the HTML code for the element, such as the text for a text area, button, or link.<br/>In addition to HTML code, you can edit and inject custom JavaScript.<br/>Several rich text formatting options are available when editing text and HTML for [!UICONTROL A/B] and [!UICONTROL Experience Targeting] activities. You can choose a font, select a font style, change text alignment, and other standard text formatting options. When modifying HTML, you can toggle between the code view and rich-editing view of the HTML.|
||Background Color|Use the color picker to select or configure a background color. You can select a color swatch, and adjust it using RGB values or color hex codes. The red x in the color picker makes the background transparent.<br/> **Note:** This option is not available for an element where a background image is set.|
||CSS Class|Specify the predefined CSS class used for the element. If more than one element is selected, separate multiple CSS classes with a space.<br/>Available for [!UICONTROL A/B], [!UICONTROL Automated Personalization], and [!UICONTROL Multivariate Test] activities.|
||Link|Change the URL in the link.<br/>Use Edit Link to update the selector to point to the same image element. However, linking to a different image element is not supported. To link to a different image element, delete the original action from the code editor and use the [!UICONTROL Visual Experience Composer] to apply the action on the other image element.|
|Insert Before|Image HTML Text|Add any kind of element to your page in addition to modifying existing content. Add text, code, lists, and more to create entirely different experiences to test.<br/>Select an element on the page, then click [!UICONTROL Insert Before] and choose whether you want to insert an image, HTML, or text. The inserted element appears before the selected element.<br/>The behavior of the inserted element depends on the structure of your page, your CSS, and other page configuration options. Valid HTML is required to make your page appear correctly. Always test your page after inserting an item to make sure it appears as expected.<br/>[!UICONTROL Recommendations] supports [!UICONTROL Insert Before] the contents of DIV, SECTION, and ARTICLE tags.<br/>**Note:** Inserting an image requires that [!DNL Adobe Scene7 Publishing System] is enabled so you have access to the image library.|
|Insert After|Image HTML Text|Add any kind of element to your page in addition to modifying existing content. Add text, code, lists, and more to create entirely different experiences to test.<br/>Select an element on the page, then click [!UICONTROL Insert After] and choose whether you want to insert an image, HTML, or text. The inserted element appears after the selected element.<br/>The behavior of the inserted element depends on the structure of your page, your CSS, and other page configuration options. Valid HTML is required to make your page appear correctly. Always test your page after inserting an item to make sure it appears as expected.<br/>[!UICONTROL Recommendations] supports [!UICONTROL Insert After] the contents of DIV, SECTION, and ARTICLE tags.<br/>**Note:** Inserting an image requires that [!DNL Adobe Scene7 Publishing System] is enabled so you have access to the image library.|
|Replace With|Image|Select a different image from the Content Library. The images available for swapping include the images uploaded to the Experience Cloud assets folder or uploaded in the Content Library in Target.<br/>During initial activity creation, the URL displayed is not the URL used for delivery. Upon activity synching, that URL is updated to a production Scene7 URL.<br/>For example, the initial URL might look like the following example:<br/>`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`<br/>After activity syncing, the delivery URL might look like the following example:<br/>`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`<br/>Recommendations supports Replace With in DIV, SECTION, and ARTICLE tags.<br/>**Note:** Swapping images requires an Adobe Scene7 Publishing System Account.|
||HTML Offer|Select a different offer from the [!UICONTROL Content Library].<br/>**Note:** HTML Offers are stored on [!DNL Target] servers.<br/>An HTML offer can be up to 256KB in size.|
||Experience Fragment|Insert experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization. For more information, see [AEM Experience Fragments](/help/c-experiences/c-manage-content/aem-experience-fragments.md).|
|Layout|Rearrange|Drag the element to another location inside the same parent element or DIV. Other elements shift location to make space for the rearranged element.<br/>**Note:** Click tracking does not work on rearranged items.|
||Resize|Resize an element on your page. When you select [!UICONTROL Resize], a handle appears in the bottom right corner of the element that lets you drag that corner to resize. Hold the Shift key to retain the same aspect ratio.<br/>**Note:** Inline elements cannot be resized.|
||Move|Move elements on your page. Unlike the [!UICONTROL Rearrange] option, [!UICONTROL Move] does not shift other elements to make room for the element being moved. Use the arrow keys to fine tune the move. (Planned enhancement: support for making sure moved elements are not hidden behind other elements.)<br/>In some cases, such as when a CSS restriction requires an element to remain inside its parent element, you cannot move the element outside its parent.|
||Hide|Hide the element. The white space remains, but the content is removed.|
||Remove|Remove the element. The white space behind the image is removed and the space where the element was is collapsed.<br/>**Note:** Items within a "classic" mbox (an mbox created within a Target Classic campaign) cannot be removed using this option.|
|Expand Selection|N/A|Select the parent element in addition to the originally selected element. When you select any parent element, all children of that element are automatically selected. You can expand the selection multiple times.|
|Navigate to this Link|N/A|Open the destination of the link.|
|Undo/Redo|N/A|Undo changes you make to your activities during an editing session. You can also redo changes that have been previously undone.|