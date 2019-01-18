---
title: Recordset.Restartable プロパティ (DAO)
TOCTitle: Restartable Property
ms:assetid: 00def49d-ea7e-6cd5-2f4a-914a1ddcdd51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844737(v=office.15)
ms:contentKeyID: 48542919
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052926
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5142d0d47be37ca8c2e1c6b89462c05b7d41d302
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721697"
---
# <a name="recordsetrestartable-property-dao"></a>Recordset.Restartable プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

**[Recordset](recordset-object-dao.md)** オブジェクトの基になるクエリを再実行する **[Requery](recordset-requery-method-dao.md)** メソッドを、 **Recordset** オブジェクトがサポートするかどうかを示す値を取得します。

## <a name="syntax"></a>構文

*式*です。再開可能

*式***レコード セット**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

テーブル タイプの **Recordset** オブジェクトは、常に **False** を返します。

**Recordset** オブジェクトに対して **Requery** メソッドを使用する前に、 **Restartable** プロパティを確認します。そのオブジェクトの **Restartable** プロパティが **False** に設定されている場合は、基になる **[QueryDef](connection-openrecordset-method-dao.md)** オブジェクトの **[OpenRecordset](querydef-object-dao.md)** メソッドを使用してクエリを再実行します。

## <a name="example"></a>例

以下の例は、さまざまな **Recordset** オブジェクトの **Restartable** プロパティの機能を示します。

```vb
    Sub RestartableX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTemp As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open a table-type Recordset and print its 
     ' Restartable property. 
     Set rstTemp = .OpenRecordset("Employees", dbOpenTable) 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from an SQL statement and print its 
     ' Restartable property. 
     Set rstTemp = _ 
     .OpenRecordset("SELECT * FROM Employees") 
     Debug.Print "Recordset based on SQL statement" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from a saved QueryDef object and 
     ' print its Restartable property. 
     Set rstTemp = .OpenRecordset("Current Product List") 
     Debug.Print _ 
     "Recordset based on permanent QueryDef (" & _ 
     rstTemp.Name & ")" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     .Close 
     End With 
     
    End Sub
```
