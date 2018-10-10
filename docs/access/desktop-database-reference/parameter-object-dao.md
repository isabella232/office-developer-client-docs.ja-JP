---
title: Parameter オブジェクト (DAO)
TOCTitle: Parameter Object
ms:assetid: 194efd23-6086-13ac-beb9-c2aec101d6fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845640(v=office.15)
ms:contentKeyID: 48543495
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 69388834d5469c9fa66d70d397d63be4376db218
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479397"
---
# <a name="parameter-object-dao"></a>Parameter オブジェクト (DAO)


**適用されます**Access 2013 |。Office 2013

**Parameter** オブジェクトは、クエリに指定する値を表します。パラメーターは、パラメーター クエリを基に作成した **QueryDef** オブジェクトに関連付けられています。

## <a name="remarks"></a>注釈

**Parameter** オブジェクトを使用すると、クエリを再コンパイルしなくても、頻繁に実行される **QueryDef** オブジェクトの引数を変更できます。

**Parameter** オブジェクトのプロパティを使用すると、変更できるクエリ パラメーターをクエリの実行前に設定できます。以下の操作を実行できます。

  - **Name** プロパティを使用して、パラメーターの名前を取得します。

  - **Value** プロパティを使用して、クエリで使用されるパラメーター値を設定または取得します。

  - **Type** プロパティを使用して、 **Parameter** オブジェクトのデータ型を取得します。

  - **Direction** プロパティを使用して、パラメーターが入力パラメーター、出力パラメーター、その両方のいずれかであるかを設定または取得します。

## <a name="example"></a>例

次の使用例は、 **Parameter** オブジェクトおよび **Parameters** コレクションの動作を、一時的な **QueryDef** オブジェクトを作成し、 **QueryDef** オブジェクトの **Parameters** に対する変更に基づいてデータを取得することで示します。このプロシージャを実行するには、ParametersChange プロシージャが必要です。

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
