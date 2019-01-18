---
title: パラメーター オブジェクト (DAO)
TOCTitle: Parameter Object
ms:assetid: 194efd23-6086-13ac-beb9-c2aec101d6fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845640(v=office.15)
ms:contentKeyID: 48543495
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5df04b1ee06a2224db9e21f67e9c68a3ee5740bf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698100"
---
# <a name="parameter-object-dao"></a><span data-ttu-id="04bef-102">パラメーター オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="04bef-102">Parameter object (DAO)</span></span>


<span data-ttu-id="04bef-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="04bef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04bef-p101">**Parameter** オブジェクトは、クエリに指定する値を表します。パラメーターは、パラメーター クエリを基に作成した **QueryDef** オブジェクトに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="04bef-p101">A **Parameter** object represents a value supplied to a query. The parameter is associated with a **QueryDef** object created from a parameter query.</span></span>

## <a name="remarks"></a><span data-ttu-id="04bef-106">注釈</span><span class="sxs-lookup"><span data-stu-id="04bef-106">Remarks</span></span>

<span data-ttu-id="04bef-107">**Parameter** オブジェクトを使用すると、クエリを再コンパイルしなくても、頻繁に実行される **QueryDef** オブジェクトの引数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="04bef-107">**Parameter** objects allow you to change the arguments in a frequently run **QueryDef** object without having to recompile the query.</span></span>

<span data-ttu-id="04bef-p102">**Parameter** オブジェクトのプロパティを使用すると、変更できるクエリ パラメーターをクエリの実行前に設定できます。以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="04bef-p102">Using the properties of a **Parameter** object, you can set a query parameter that can be changed before the query is run. You can:</span></span>

  - <span data-ttu-id="04bef-110">**Name** プロパティを使用して、パラメーターの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="04bef-110">Use the **Name** property to return the name of a parameter.</span></span>

  - <span data-ttu-id="04bef-111">**Value** プロパティを使用して、クエリで使用されるパラメーター値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="04bef-111">Use the **Value** property to set or return the parameter values to be used in the query.</span></span>

  - <span data-ttu-id="04bef-112">**Type** プロパティを使用して、 **Parameter** オブジェクトのデータ型を取得します。</span><span class="sxs-lookup"><span data-stu-id="04bef-112">Use the **Type** property to return the data type of the **Parameter** object.</span></span>

  - <span data-ttu-id="04bef-113">**Direction** プロパティを使用して、パラメーターが入力パラメーター、出力パラメーター、その両方のいずれかであるかを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="04bef-113">Use the **Direction** property to set or return whether the parameter is an input parameter, an output parameter, or both.</span></span>

## <a name="example"></a><span data-ttu-id="04bef-114">例</span><span class="sxs-lookup"><span data-stu-id="04bef-114">Example</span></span>

<span data-ttu-id="04bef-p103">次の使用例は、 **Parameter** オブジェクトおよび **Parameters** コレクションの動作を、一時的な **QueryDef** オブジェクトを作成し、 **QueryDef** オブジェクトの **Parameters** に対する変更に基づいてデータを取得することで示します。このプロシージャを実行するには、ParametersChange プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="04bef-p103">This example demonstrates **Parameter** objects and the **Parameters** collection by creating a temporary **QueryDef** and retrieving data based on changes made to the **QueryDef** object's **Parameters**. The ParametersChange procedure is required for this procedure to run.</span></span>

```vb
    Sub ParameterX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfReport As QueryDef 
     Dim prmBegin As Parameter 
     Dim prmEnd As Parameter 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create temporary QueryDef object with two 
     ' parameters. 
     Set qdfReport = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS dteBegin DateTime, dteEnd DateTime; " & _ 
     "SELECT EmployeeID, COUNT(OrderID) AS NumOrders " & _ 
     "FROM Orders WHERE ShippedDate BETWEEN " & _ 
     "[dteBegin] AND [dteEnd] GROUP BY EmployeeID " & _ 
     "ORDER BY EmployeeID") 
     Set prmBegin = qdfReport.Parameters!dteBegin 
     Set prmEnd = qdfReport.Parameters!dteEnd 
     
     ' Print report using specified parameter values. 
     ParametersChange qdfReport, prmBegin, #1/1/95#, _ 
     prmEnd, #6/30/95# 
     ParametersChange qdfReport, prmBegin, #7/1/95#, _ 
     prmEnd, #12/31/95# 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub ParametersChange(qdfTemp As QueryDef, _ 
     prmFirst As Parameter, dteFirst As Date, _ 
     prmLast As Parameter, dteLast As Date) 
     ' Report function for ParameterX. 
     
     Dim rstTemp As Recordset 
     Dim fldLoop As Field 
     
     ' Set parameter values and open recordset from 
     ' temporary QueryDef object. 
     prmFirst = dteFirst 
     prmLast = dteLast 
     Set rstTemp = _ 
     qdfTemp.OpenRecordset(dbOpenForwardOnly) 
     Debug.Print "Period " & dteFirst & " to " & dteLast 
     
     ' Enumerate recordset. 
     Do While Not rstTemp.EOF 
     
     ' Enumerate Fields collection of recordset. 
     For Each fldLoop In rstTemp.Fields 
     Debug.Print " - " & fldLoop.Name & " = " & fldLoop; 
     Next fldLoop 
     
     Debug.Print 
     rstTemp.MoveNext 
     Loop 
     
     rstTemp.Close 
     
    End Sub
```
