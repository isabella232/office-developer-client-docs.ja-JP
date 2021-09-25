---
title: QueryDef.RecordsAffected プロパティ (DAO)
TOCTitle: RecordsAffected Property
ms:assetid: 29a864b5-305c-d33f-b2ca-fc9a08baaa5c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192040(v=office.15)
ms:contentKeyID: 48543886
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053082
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 7b3d97c433750a42f34a65ee49d020aebe11ad50
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577004"
---
# <a name="querydefrecordsaffected-property-dao"></a>QueryDef.RecordsAffected プロパティ (DAO)


**適用先:** Access 2013、Office 2013

最後に呼び出した **[Execute](querydef-execute-method-dao.md)** メソッドの処理対象となったレコードの数を取得します。

## <a name="syntax"></a>構文

*式* .RecordsAffected

*式* **QueryDef** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**Execute** メソッドを使用して **QueryDef** オブジェクトからアクション クエリを実行すると、削除、更新、または挿入されたレコードの数が **RecordsAffected** プロパティに格納されます。

## <a name="example"></a>例

この例では、 [**Database**](database-object-dao.md) オブジェクトおよび **QueryDef** オブジェクトから実行するアクション クエリで **RecordsAffected** プロパティを使用します。このプロシージャを実行するには、RecordsAffectedOutput 関数が必要です。

```vb
    Sub RecordsAffectedX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim strSQLChange As String 
     Dim strSQLRestore As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Print report of contents of the Employees 
     ' table. 
     Debug.Print _ 
     "Number of records in Employees table: " & _ 
     .TableDefs!Employees.RecordCount 
     RecordsAffectedOutput dbsNorthwind 
     
     ' Define and execute an action query. 
     strSQLChange = "UPDATE Employees " & _ 
     "SET Country = 'United States' " & _ 
     "WHERE Country = 'USA'" 
     .Execute strSQLChange 
     
     ' Print report of contents of the Employees 
     ' table. 
     Debug.Print _ 
     "RecordsAffected after executing query " & _ 
     "from Database: " & .RecordsAffected 
     RecordsAffectedOutput dbsNorthwind 
     
     ' Define and run another action query. 
     strSQLRestore = "UPDATE Employees " & _ 
     "SET Country = 'USA' " & _ 
     "WHERE Country = 'United States'" 
     Set qdfTemp = .CreateQueryDef("", strSQLRestore) 
     qdfTemp.Execute 
     
     ' Print report of contents of the Employees 
     ' table. 
     Debug.Print _ 
     "RecordsAffected after executing query " & _ 
     "from QueryDef: " & qdfTemp.RecordsAffected 
     RecordsAffectedOutput dbsNorthwind 
     
     .Close 
     
     End With 
     
    End Sub 
     
    Function RecordsAffectedOutput(dbsNorthwind As Database) 
     
     Dim rstEmployees As Recordset 
     
     ' Open a Recordset object from the Employees table. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Enumerate Recordset. 
     .MoveFirst 
     Do While Not .EOF 
     Debug.Print " " & !LastName & ", " & !Country 
     .MoveNext 
     Loop 
     .Close 
     End With 
     
    End Function
```
