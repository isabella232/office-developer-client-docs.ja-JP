---
title: Recordset2.Restartable プロパティ (DAO)
TOCTitle: Restartable Property
ms:assetid: 9b1c40f8-5a33-2527-a7b6-bef4cb991d7e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198019(v=office.15)
ms:contentKeyID: 48546560
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c85be857f7a7ed100e68f77f954b3d7513449fa5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870213"
---
# <a name="recordset2restartable-property-dao"></a>Recordset2.Restartable プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

**[Recordset](recordset-object-dao.md)** オブジェクトの基になるクエリを再実行する **[Requery](recordset2-requery-method-dao.md)** メソッドを、 **Recordset** オブジェクトがサポートするかどうかを示す値を取得します。

## <a name="syntax"></a>構文

*式*です。再開可能

*式***Recordset2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

テーブル タイプの **Recordset** オブジェクトは、常に **False** を返します。

**Recordset** オブジェクトに対して **Requery** メソッドを使用する前に、 **Restartable** プロパティを確認します。そのオブジェクトの **Restartable** プロパティが **False** に設定されている場合は、基になる **[QueryDef](connection-openrecordset-method-dao.md)** オブジェクトの **[OpenRecordset](querydef-object-dao.md)** メソッドを使用してクエリを再実行します。

## <a name="example"></a>例

以下の例は、さまざまな **Recordset** オブジェクトの **Restartable** プロパティの機能を示します。

```vb
    Sub RestartableX()
    
       Dim dbsNorthwind As Database
       Dim rstTemp As Recordset2
    
       Set dbsNorthwind = OpenDatabase("Northwind.mdb")
    
       With dbsNorthwind
          ' Open a table-type Recordset and print its 
          ' Restartable property.
          Set rstTemp = .OpenRecordset("Employees", dbOpenTable)
          Debug.Print _
             "Table-type recordset from Employees table"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          ' Open a Recordset from an SQL statement and print its 
          ' Restartable property.
          Set rstTemp = _
             .OpenRecordset("SELECT * FROM Employees")
          Debug.Print "Recordset based on SQL statement"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          ' Open a Recordset from a saved QueryDef object and 
          ' print its Restartable property.
          Set rstTemp = .OpenRecordset("Current Product List")
          Debug.Print _
             "Recordset based on permanent QueryDef (" & _
             rstTemp.Name & ")"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          .Close
       End With
    
    End Sub
```
