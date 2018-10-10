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
ms.openlocfilehash: 9377f61ec334f41b7f8ccba61b87a9d5953b4429
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478519"
---
# <a name="querydefrecordsaffected-property-dao"></a><span data-ttu-id="c1c1e-102">QueryDef.RecordsAffected プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="c1c1e-102">QueryDef.RecordsAffected Property (DAO)</span></span>


<span data-ttu-id="c1c1e-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1c1e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c1c1e-104">直前に呼び出された **[Execute](querydef-execute-method-dao.md)** メソッドの影響を受けるレコード数を返します。</span><span class="sxs-lookup"><span data-stu-id="c1c1e-104">Returns the number of records affected by the most recently invoked **[Execute](querydef-execute-method-dao.md)** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c1e-105">構文</span><span class="sxs-lookup"><span data-stu-id="c1c1e-105">Syntax</span></span>

<span data-ttu-id="c1c1e-106">*式*です。RecordsAffected</span><span class="sxs-lookup"><span data-stu-id="c1c1e-106">*expression* .RecordsAffected</span></span>

<span data-ttu-id="c1c1e-107">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="c1c1e-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1c1e-108">注釈</span><span class="sxs-lookup"><span data-stu-id="c1c1e-108">Remarks</span></span>

<span data-ttu-id="c1c1e-109">**Execute** メソッドを使用して **QueryDef** オブジェクトからアクション クエリを実行すると、削除、更新、または挿入されたレコードの数が **RecordsAffected** プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="c1c1e-109">When you use the **Execute** method to run an action query from a **QueryDef** object, the **RecordsAffected** property will contain the number of records deleted, updated, or inserted.</span></span>

## <a name="example"></a><span data-ttu-id="c1c1e-110">例</span><span class="sxs-lookup"><span data-stu-id="c1c1e-110">Example</span></span>

<span data-ttu-id="c1c1e-p101">この例では、 [**Database**](database-object-dao.md) オブジェクトおよび **QueryDef** オブジェクトから実行するアクション クエリで **RecordsAffected** プロパティを使用します。このプロシージャを実行するには、RecordsAffectedOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="c1c1e-p101">This example uses the **RecordsAffected** property with action queries executed from a **[Database](database-object-dao.md)** object and from a **QueryDef** object. The RecordsAffectedOutput function is required for this procedure to run.</span></span>

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