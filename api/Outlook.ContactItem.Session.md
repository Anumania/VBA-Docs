---
title: ContactItem.Session property (Outlook)
keywords: vbaol11.chm928
f1_keywords:
- vbaol11.chm928
ms.prod: outlook
api_name:
- Outlook.ContactItem.Session
ms.assetid: b67eb0d4-9b97-2be7-fc24-ecdd58fb01ca
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# ContactItem.Session property (Outlook)

Returns the  **[NameSpace](Outlook.NameSpace.md)** object for the current session. Read-only.


## Syntax

_expression_.**Session**

_expression_ A variable that represents a [ContactItem](Outlook.ContactItem.md) object.


## Remarks

The **Session** property and the **[GetNamespace](Outlook.Application.GetNamespace.md)** method can be used interchangeably to obtain the **NameSpace** object for the current session. Both members serve the same purpose. For example, the following statements do the same function:


```vb
Set objNamespace = Application.GetNamespace("MAPI") 
```


```vb
Set objSession = Application.Session
```


## See also


[ContactItem Object](Outlook.ContactItem.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]