---
title: DocumentItem.BeforeCheckNames event (Outlook)
ms.prod: outlook
api_name:
- Outlook.DocumentItem.BeforeCheckNames
ms.assetid: 0798f1bc-4a7e-7f85-0719-31f5f937cfc3
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# DocumentItem.BeforeCheckNames event (Outlook)

Occurs just before Microsoft Outlook starts resolving names in the recipient collection for an item (which is an instance of the parent object).


## Syntax

_expression_. `BeforeCheckNames`( `_Cancel_` )

_expression_ A variable that represents a [DocumentItem](Outlook.DocumentItem.md) object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Cancel_|Required| **Boolean**| **False** when the event occurs. If the event procedure sets this argument to **True**, the name resolution process is not completed.|

## Remarks

You use the  **BeforeCheckNames** event in VBScript, but the event does not fire when an email name is resolved on the form.

The event does not fire under the following circumstances:


- You customized a Journal Entry form and then resolved a contact in the  **Contacts** field.
    
- You customized a Contact form and then resolved a contact in the  **Contacts** field.
    
- You customized any type of form and Outlook automatically resolved the name in the background.
    
- You programmatically created and resolved a recipient.
    



## See also


[DocumentItem Object](Outlook.DocumentItem.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]