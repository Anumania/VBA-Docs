---
title: ToolbarSet.SetID property (Visio)
keywords: vis_sdr.chm13914315
f1_keywords:
- vis_sdr.chm13914315
ms.prod: visio
api_name:
- Visio.ToolbarSet.SetID
ms.assetid: db1f1cf5-f9eb-a118-132d-9ac878db6632
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# ToolbarSet.SetID property (Visio)

Returns the set ID of an  **ToolbarSet** object in its collection. Read-only.


## Syntax

_expression_.**SetID**

_expression_ A variable that represents a **[ToolbarSet](Visio.ToolbarSet.md)** object.


## Return value

Long


## Remarks


> [!NOTE] 
> Starting with Visio 2010, the Microsoft Office Fluent user interface (UI) replaced the previous system of layered menus, toolbars, and task panes. VBA objects and members that you used to customize the user interface in previous versions of Visio are still available in Visio, but they function differently.

Each  **ToolbarSet** object has a set ID that corresponds to a Microsoft Visio window context. For **ToolbarSet** objects, they also correspond to drop-down menus under toolbar buttons (such as **Fill Color** or **Line Weight**).

You can retrieve an object from its collection by passing the object's set ID to the  **ItemAtID** property. You can also set the set ID of an object by using the **AddAtID** method.

Valid set ID values are declared by the Visio type library in  **[VisUIObjSets](Visio.visuiobjsets.md)**.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]