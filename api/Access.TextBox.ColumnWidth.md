---
title: TextBox.ColumnWidth property (Access)
keywords: vbaac10.chm11095
f1_keywords:
- vbaac10.chm11095
ms.prod: access
api_name:
- Access.TextBox.ColumnWidth
ms.assetid: 19060aac-ccb0-3998-39c7-42f1454c339e
ms.date: 02/21/2019
ms.localizationpriority: medium
---


# TextBox.ColumnWidth property (Access)

You can use the **ColumnWidth** property to specify the width of a column in Datasheet view. Read/write **Integer**.


## Syntax

_expression_.**ColumnWidth**

_expression_ A variable that represents a **[TextBox](Access.TextBox.md)** object.


## Remarks

In Visual Basic, the **ColumnWidth** property setting is an **Integer** value that represents the column width in [twips](../language/glossary/vbe-glossary.md#twip). You can specify a width or use one of the following predefined settings.

|Setting|Description|
|:-----|:-----|
|0|Hides the column.|
|-1|(Default) Sizes the column to the default width.|
|-2|Sizes the column to fit the width of the displayed text.|


The **ColumnWidth** property applies to all fields in Datasheet view and to form controls when the form is in Datasheet view.

Setting this property to 0, or resizing the field to a zero width in Datasheet view, sets the field's **ColumnHidden** property to **True** (-1) and hides the field in Datasheet view.

Setting a field's **ColumnHidden** property to **False** (0) restores the field's **ColumnWidth** property to the value it had before the field was hidden. For example, if the **ColumnWidth** property was 1 prior to the field being hidden by setting the property to 0, changing the field's **ColumnHidden** property to **False** resets the **ColumnWidth** to 1.

Setting the **ColumnWidth** property for a field when the field's **ColumnHidden** property is set to **True** has no effect.


## Example

This example takes effect in Datasheet view of the open **Customers** form. It sets the row height to 450 twips and sizes the column to fit the size of the visible text.

```vb
Forms![Customers].RowHeight = 450 
Forms![Customers]![Address].ColumnWidth = -2
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
