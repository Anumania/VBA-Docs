---
title: Printer.DataOnly property (Access)
keywords: vbaac10.chm12871
f1_keywords:
- vbaac10.chm12871
ms.prod: access
api_name:
- Access.Printer.DataOnly
ms.assetid: 2df339fe-140a-374f-01cf-d1d93ed87fee
ms.date: 03/23/2019
ms.localizationpriority: medium
---


# Printer.DataOnly property (Access)

**True** if Microsoft Access prints only the data from a table or query in Datasheet view and not the labels, control borders, gridlines, and display graphics. Read/write **Boolean**.


## Syntax

_expression_.**DataOnly**

_expression_ A variable that represents a **[Printer](Access.Printer.md)** object.


## Example

The following example sets a variety of printer settings for the form specified in the _strFormname_ argument of the procedure.

```vb
Sub SetPrinter(strFormname As String) 
 
 DoCmd.OpenForm FormName:=strFormname, view:=acDesign, _ 
 datamode:=acFormEdit, windowmode:=acHidden 
 
 With Forms(form1).Printer 
 
 .TopMargin = 1440 
 .BottomMargin = 1440 
 .LeftMargin = 1440 
 .RightMargin = 1440 
 
 .ColumnSpacing = 360 
 .RowSpacing = 360 
 
 .ColorMode = acPRCMColor 
  .DataOnly = False 
 .DefaultSize = False 
 .ItemSizeHeight = 2880 
 .ItemSizeWidth = 2880 
 .ItemLayout = acPRVerticalColumnLayout 
 .ItemsAcross = 6 
 
 .Copies = 1 
 .Orientation = acPRORLandscape 
 .Duplex = acPRDPVertical 
 .PaperBin = acPRBNAuto 
 .PaperSize = acPRPSLetter 
 .PrintQuality = acPRPQMedium 
 
 End With 
 
 DoCmd.Close objecttype:=acForm, objectname:=strFormname, _ 
 Save:=acSaveYes 
 
 
End Sub
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]