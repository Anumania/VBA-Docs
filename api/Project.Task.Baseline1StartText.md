---
title: Task.Baseline1StartText property (Project)
ms.prod: project-server
api_name:
- Project.Task.Baseline1StartText
ms.assetid: e2f078df-ee31-a2e2-4ee4-512b236c9fb2
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Task.Baseline1StartText property (Project)

Gets or sets a string representation of the baseline start date of a task. Read/write  **String**.


## Syntax

_expression_. `Baseline1StartText`

 _expression_ An expression that returns a [Task](./Project.Task.md) object.


## Remarks

The **Baseline1StartText** property is used for manually scheduled tasks. When you convert a manually scheduled task to an auto-scheduled task, if **Baseline1StartText** has any value, you should convert the value to a date for the **Baseline1Start** property.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]