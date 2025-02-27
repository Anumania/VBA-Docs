---
title: OlkComboBox.BeforeUpdate event (Outlook)
keywords: vbaol11.chm1000248
f1_keywords:
- vbaol11.chm1000248
ms.prod: outlook
api_name:
- Outlook.OlkComboBox.BeforeUpdate
ms.assetid: f9c6620e-22ce-c4cb-8dc1-7a99bc8d508b
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# OlkComboBox.BeforeUpdate event (Outlook)

Occurs when the data in the control is changed through the user interface and is about to be saved to the item. 


## Syntax

_expression_.**BeforeUpdate** (_Cancel_)

_expression_ A variable that represents an [OlkComboBox](Outlook.OlkComboBox.md) object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Cancel_|Required| **Boolean**| **False** when the event occurs. If the event procedure sets this argument to **True**, the operation will not be completed and the property bound to the control will not be updated.|

## Remarks

Canceling this property will revert the control to the current value of the property and return the focus to the control.

 **BeforeUpdate** and **AfterUpdate** can occur any time the data in the control is being saved to the item. The typical sequence of events involving **BeforeUpdate** for this control is as follows:


1. User focuses on the control
    
2.  **BeforeUpdate**
    
3. Control data is updated
    
4.  ** AfterUpdate**
    
5.  **Exit** : User moves focus away from control
    



## See also


[OlkComboBox Object](Outlook.OlkComboBox.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]