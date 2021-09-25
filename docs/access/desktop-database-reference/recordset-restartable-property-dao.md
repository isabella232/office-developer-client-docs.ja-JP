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
ms.localizationpriority: medium
ms.openlocfilehash: e0af1932a625703c08f7b0c873c177e21bd14ed0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572880"
---
# <a name="recordsetrestartable-property-dao"></a>Recordset.Restartable プロパティ (DAO)


**適用先:** Access 2013、Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクトの基になるクエリを再実行する **[Requery](recordset-requery-method-dao.md)** メソッドを、 **Recordset** オブジェクトがサポートするかどうかを示す値を取得します。

## <a name="syntax"></a>構文

*式* .再起動可能

*expression*: **Recordset** オブジェクトを表す変数。

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
