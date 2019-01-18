---
title: Field2.DataUpdatable プロパティ (DAO)
TOCTitle: DataUpdatable Property
ms:assetid: e6619c4e-26b1-777b-f0de-78fed3dbc890
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835966(v=office.15)
ms:contentKeyID: 48548377
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 88a57ff2daeaaaab202daad55f01eebc6bdf86dd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698960"
---
# <a name="field2dataupdatable-property-dao"></a>Field2.DataUpdatable プロパティ (DAO)


**適用されます**Access 2013、Office 2013。


**Field2** オブジェクトで表されるフィールドのデータが更新可能かどうかを示す値を返します。

## <a name="syntax"></a>構文

*式*です。DataUpdatable

*式***Field2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

このプロパティを使用して、 [Field2](field-value-property-dao.md) オブジェクトの ****Value**** プロパティの設定値が変更可能かどうかを識別します。このプロパティは、 ****Attributes**** プロパティが [dbAutoIncrField](field-attributes-property-dao.md) の **Field2** オブジェクトでは常に **False** です。

DataUpdatable プロパティは、QueryDef、Recordset、および Relation の各オブジェクトの Fields コレクションに追加される Field2 オブジェクトでは使用できますが、Index オブジェクトまたは TableDef オブジェクトの Fields コレクションに追加される Field2 オブジェクトでは使用できません。

## <a name="example"></a>例

次の使用例では、6 つの異なる **Recordsets** オブジェクトの最初のフィールドを使用して **DataUpdatable** プロパティを示します。このプロシージャを実行するには、DataOutput 関数が必要です。

```vb 
Sub DataUpdatableX() 
 
 Dim dbsNorthwind As Database 
 Dim rstNorthwind As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Open and print report about a table-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a dynaset-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenDynaset) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a snapshot-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenSnapshot) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a forward-only-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenForwardOnly) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on 
 ' a select query. 
 Set rstNorthwind = _ 
 .OpenRecordset("Current Product List") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on a 
 ' select query that calculates totals. 
 Set rstNorthwind = .OpenRecordset("Order Subtotals") 
 DataOutput rstNorthwind 
 
 .Close 
 End With 
 
End Sub 
 
Function DataOutput(rstTemp As Recordset) 
 
 With rstTemp 
 Debug.Print "Recordset: " & .Name & ", "; 
 Select Case .Type 
 Case dbOpenTable 
 Debug.Print "dbOpenTable" 
 Case dbOpenDynaset 
 Debug.Print "dbOpenDynaset" 
 Case dbOpenSnapshot 
 Debug.Print "dbOpenSnapshot" 
 Case dbOpenForwardOnly 
 Debug.Print "dbOpenForwardOnly" 
 End Select 
 Debug.Print " Field: " & .Fields(0).Name & ", " & _ 
 "DataUpdatable = " & .Fields(0).DataUpdatable 
 Debug.Print 
 .Close 
 End With 
 
End Function 
 
```

