---
title: IVBUndoUnit.UnitTypeCLSID property (Visio)
keywords: vis_sdr.chm17360170
f1_keywords:
- vis_sdr.chm17360170
ms.prod: visio
api_name:
- Visio.IVBUndoUnit.UnitTypeCLSID
ms.assetid: 7b75de4d-5119-d7a9-fec2-626807ab68b6
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# IVBUndoUnit.UnitTypeCLSID property (Visio)

Identifies an undo unit by its class ID (CLSID). Read-only.


## Syntax

_expression_. `UnitTypeCLSID`

_expression_ A variable that represents an **[IVBUndoUnit](visio.ivbundounit.md)** object.


## Return value

String


## Remarks

If you are creating an undo unit for your solution, the  **UnitTypeCLSID** property is one of the members of **IVBUndoUnit** that you must implement. You can use the **UnitTypeCLSID** value to identify your undo units. You can use the same CLSID for multiple undo units and use different values in the **UnitTypeLong** property.

The  **UnitTypeCLSID** value is optional, and you can set the value to **Nothing** or to an empty string when you implement the property.

For more information about the  **UnitTypeCLSID** property and using the **IVBUndoUnit** interface to create undo units, search for "creating undo units" on MSDN.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]