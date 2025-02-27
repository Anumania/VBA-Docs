---
title: ListBox.IMEHold property (Access)
keywords: vbaac10.chm11229
f1_keywords:
- vbaac10.chm11229
ms.prod: access
api_name:
- Access.ListBox.IMEHold
ms.assetid: 22d6bd7c-704b-2b27-6b04-c6628cd83f02
ms.date: 03/01/2019
ms.localizationpriority: medium
---


# ListBox.IMEHold property (Access)

You can use the **IMEHold/Hold KanjiConversionMode** property to show whether the Kanji Conversion Mode is maintained when the control loses the focus. Read/write **Boolean**.


## Syntax

_expression_.**IMEHold**

_expression_ A variable that represents a **[ListBox](Access.ListBox.md)** object.


## Remarks

The **IMEHold/Hold KanjiConversionMode** property uses the following settings.

|Setting|Description|
|:-----|:-----|
|**True**|Maintains the Kanji Conversion Mode set in the last control.|
|**False**|Does not maintain the Kanji Conversion Mode set in the last control (default).|

By setting the **IMEMode/KanjiConversionMode** property, you can designate whether the Kanji Conversion Mode is maintained when the control loses the focus. 

If this property is set to Yes, the Kanji Conversion Mode setting is maintained when the control loses the focus. After that control regains the focus, the Kanji Conversion Mode setting for that control is restored. 

If this property is set to No (default setting), the Kanji Conversion Mode will be set by the **IMEMode/KanjiConversionMode** property for that control.

> [!NOTE] 
> To set the Kanji Conversion Mode when the focus shifts to the control, set the **IMEMode/KanjiConversionMode** property.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]