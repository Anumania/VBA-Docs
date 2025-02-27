---
title: FormatCondition.Expression2 property (Access)
keywords: vbaac10.chm10061
f1_keywords:
- vbaac10.chm10061
ms.prod: access
api_name:
- Access.FormatCondition.Expression2
ms.assetid: e251c8b7-3d7a-961f-2d46-ec58ea3f4b0b
ms.date: 03/20/2019
ms.localizationpriority: medium
---


# FormatCondition.Expression2 property (Access)

You can use the **Expression2** property to return the values of a conditional format within a **FormatCondition** object. Read-only **String**.


## Syntax

_expression_.**Expression2**

_expression_ A variable that represents a **[FormatCondition](Access.FormatCondition.md)** object.


## Remarks

The **Expression2** property returns a **Variant** value or expression associated with the second part of the conditional format when the **Operator** property of the **FormatCondition** object is **acBetween** or **acNotBetween**; otherwise, the **Expression2** property is **null**.



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]