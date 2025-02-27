---
title: Application.DStDevP method (Access)
keywords: vbaac10.chm12534
f1_keywords:
- vbaac10.chm12534
ms.prod: access
api_name:
- Access.Application.DStDevP
ms.assetid: ca5fb7ad-d91e-1222-e99a-8c55f34482f3
ms.date: 02/05/2019
ms.localizationpriority: medium
---


# Application.DStDevP method (Access)

Estimates the standard deviation across a population in a specified set of records (a domain).


## Syntax

_expression_.**DStDevP** (_Expr_, _Domain_, _Criteria_)

_expression_ A variable that represents an **[Application](Access.Application.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Expr_|Required|**String**|An expression that identifies the numeric field on which you want to find the standard deviation. It can be a string expression identifying a field from a table or query, or it can be an expression that performs a [calculation on data in that field](../access/Concepts/Criteria-Expressions/calculate-fields-in-domain-aggregate-functions.md). In _expr_, you can include the name of a field in a table, a control on a form, a constant, or a function. If _expr_ includes a function, it can be either built-in or user-defined, but not another domain aggregate or SQL aggregate function.|
| _Domain_|Required|**String**|A string expression identifying the set of records that constitutes the domain. It can be a table name or a query name for a query that does not require a parameter.|
| _Criteria_|Optional|**Variant**|An optional string expression used to restrict the range of data on which the **DStDevP** function is performed. For example, _criteria_ is often equivalent to the WHERE clause in an SQL expression, without the word WHERE. If _criteria_ is omitted, the **DStDevP** function evaluates _expr_ against the entire domain. Any field that is included in _criteria_ must also be a field in _domain_; otherwise, the **DStDevP** function will return a **Null**.|

## Return value

Variant


## Remarks

If _domain_ refers to fewer than two records, or if fewer than two records satisfy _criteria_, the **DStDevP** function returns a **Null**, indicating that a standard deviation can't be calculated.

You can use the **DStDevP** function to specify criteria in the **Criteria** row of a select query. For example, you could create a query on an Orders table and a Products table to display all products for which the freight cost fell above the mean plus the standard deviation for freight cost.

You can use the **DStDevP** function in a calculated field expression of a query, or in the **Update To** row of an update query.

> [!NOTE] 
> You can use the **DStDev** and **DStDevP** functions or the **StDev** and **StDevP** functions in a calculated field expression of a totals query. If you use the **DStDev** or **DStDevP** function, values are calculated before data is grouped. If you use the **StDev** or **StDevP** function, the data is grouped before values in the field expression are evaluated.

Use the **DStDev** function in a calculated control when you need to specify criteria to restrict the range of data on which the function is performed.

If you simply want to find the standard deviation across all records in _domain_, use the **StDev** or **StDevP** function.

If the data type of the field from which _expr_ is derived is a number, the **DStDevP** function returns a **Double** data type. If you use the **DStDevP** function in a calculated control, include a data type conversion function in the expression to improve performance.


## Example

The following example returns estimates of the standard deviation for a population and a population sample for orders shipped to the United Kingdom. The domain is an Orders table. The _criteria_ argument restricts the resulting set of records to those for which the ShipCountry value is UK.

```vb
Dim dblX As Double 
Dim dblY As Double 
 
' Sample estimate. 
dblX = DStDev("[Freight]", "Orders", "[ShipCountry] = 'UK'") 
 
' Population estimate. 
dblY = DStDevP("[Freight]", "Orders", "[ShipCountry] = 'UK'")
```

<br/>

The next example calculates the same estimates by using the variable `strCountry` in the _criteria_ argument. Note that single quotation marks (') are included in the string expression, so that when the strings are concatenated, the string literal `UK` will be enclosed in single quotation marks.

```vb
Dim strCountry As String 
Dim dblX As Double 
Dim dblY As Double 
 
strCountry = "UK" 
 
dblX = DStDev("[Freight]", "Orders", _ 
    "[ShipCountry] = '" & strCountry & "'") 
 
dblY = DStDevP("[Freight]", "Orders", _ 
    "[ShipCountry] = '" & strCountry & "'")
```

<br/>

The following examples show how to use various types of criteria with the **DStDevP** function.

```vb
    ' ***************************
    ' Typical Use
    ' Numerical values. Replace "number" with the number to use.
    variable = DStDevP("[FieldName]", "TableName", "[Criteria] = number")

    ' Strings.
    ' Numerical values. Replace "string" with the string to use.
    variable = DStDevP("[FieldName]", "TableName", "[Criteria]= 'string'")

    ' Dates. Replace "date" with the string to use.
    variable = DStDevP("[FieldName]", "TableName", "[Criteria]= #date#")
    ' ***************************

    ' ***************************
    ' Referring to a control on a form
    ' Numerical values
    variable = DStDevP("[FieldName]", "TableName", "[Criteria] = " & Forms!FormName!ControlName)

    ' Strings
    variable = DStDevP("[FieldName]", "TableName", "[Criteria] = '" & Forms!FormName!ControlName & "'")

    ' Dates
    variable = DStDevP("[FieldName]", "TableName", "[Criteria] = #" & Forms!FormName!ControlName & "#")
    ' ***************************

    ' ***************************
    ' Combinations
    ' Multiple types of criteria
    variable = DStDevP("[FieldName]", "TableName", "[Criteria1] = " & Forms![FormName]![Control1] _
             & " AND [Criteria2] = '" & Forms![FormName]![Control2] & "'" _
            & " AND [Criteria3] =#" & Forms![FormName]![Control3] & "#")
    
    ' Use two fields from a single record.
    variable = DStDevP("[LastName] & ', ' & [FirstName]", "tblPeople", "[PrimaryKey] = 7")
            
    ' Expressions
    variable = DStDevP("[Field1] + [Field2]", "tableName", "[PrimaryKey] = 7")
    
    ' Control Structures
    variable = DStDevP("IIf([LastName] Like 'Smith', 'True', 'False')", "tableName", "[PrimaryKey] = 7")
    ' ***************************
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]