---
title: Image.SpecialEffect Property (Outlook Forms Script)
ms.prod: outlook
ms.assetid: 174b4b27-a50f-da85-5ffe-91e268fce837
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Image.SpecialEffect Property (Outlook Forms Script)

Returns or sets an **Integer** that specifies the visual appearance of an object. Read/write.


## Syntax

_expression_.**SpecialEffect**

_expression_ A variable that represents an **Image** object.


## Remarks

The settings for  **SpecialEffect** are:



|Value|Description|
|:-----|:-----|
|0|Object appears flat, distinguished from the surrounding form by a border, a change of color, or both. Default for  **[Image](Outlook.image.md)**.|
|1|Object has a highlight on the top and left and a shadow on the bottom and right.|
|2|Object has a shadow on the top and left and a highlight on the bottom and right. The control and its border appear to be carved into the form that contains them.|
|3|Border appears to be carved around the edge of the control.|
|6|Object has a ridge on the bottom and right and appears flat on the top and left.|

You can use either the  **SpecialEffect** or the **[BorderStyle](Outlook.image.borderstyle.md)** property to specify the edging for a control, but not both. If you specify a nonzero value for one of these properties, the system sets the value of the other property to zero. For example, if you set **SpecialEffect** to 1, the system sets **BorderStyle** to 0.

 **SpecialEffect** uses the system colors to define its borders.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]