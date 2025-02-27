---
title: WebOptions.RelyOnVML property (Word)
keywords: vbawd10.chm165937158
f1_keywords:
- vbawd10.chm165937158
ms.prod: word
api_name:
- Word.WebOptions.RelyOnVML
ms.assetid: f8d817ee-c5f0-d11a-7156-95bd078e8633
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# WebOptions.RelyOnVML property (Word)

 **True** if image files are not generated from drawing objects when you save a document as a webpage. **False** if images are generated. The default value is **False**. Read/write **Boolean**.


## Syntax

_expression_.**RelyOnVML**

_expression_ Required. A variable that represents a **[WebOptions](Word.WebOptions.md)** collection.


## Remarks

You can reduce file sizes by not generating images for drawing objects, if your web browser supports Vector Markup Language (VML). For example, Microsoft Internet Explorer 5 supports this feature, and you should set the **RelyOnVML** property to **True** if you are targeting this browser. For browsers that do not support VML, the image will not appear when you view a webpage saved with this property enabled.

Don't generate images if your webpage uses image files that you have generated earlier and if the location where you save the document is different from the final location of the page on the web server.


## Example

This example specifies that images are generated when saving the document as a webpage.


```vb
ActiveDocument.WebOptions.RelyOnVML = False
```


## See also


[WebOptions Object](Word.WebOptions.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]