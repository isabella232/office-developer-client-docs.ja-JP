---
title: Recordset.BatchCollisionCount プロパティ (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 9d166463-8313-c0f5-8389-5d5ad933eb33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198240(v=office.15)
ms:contentKeyID: 48546617
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101181
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 079da0d4e489b4082283c78bc9e84b7d95959e82
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883310"
---
# <a name="recordsetbatchcollisioncount-property-dao"></a>Recordset.BatchCollisionCount プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

## <a name="syntax"></a>構文

*式*です。BatchCollisionCount

*式***レコード セット**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

このプロパティは、競合が発生したレコード数、または最後のバッチ更新を実行しようとしたときに更新に失敗したレコード数を示します。このプロパティの値は、 **[BatchCollisions](recordset-batchcollisions-property-dao.md)** プロパティのブックマークの数に対応します。

作業中の **[Recordset](recordset-object-dao.md)** オブジェクトの **[Bookmark](recordset-bookmark-property-dao.md)** プロパティを、 **BatchCollisions** 配列のブックマークの値に設定すると、最新のバッチ **[Update](recordset-update-method-dao.md)** 操作の完了に失敗した各レコードに移動できます。

競合するレコードを修正した後、バッチモードの **Update** メソッドを再び呼び出すことができます。ここで DAO はもう一度バッチ更新を試み、再び **BatchCollisions** プロパティに、2 回目の実行で失敗したレコードのセットが反映されます。以前の実行が正常に終了したレコードは、 **[RecordStatus](recordset-recordstatus-property-dao.md)** プロパティが dbRecordUnmodified に設定されているため、現在の実行には送信されません。このプロセスは、競合が発生する限り続行できますが、更新を中止して結果セットを閉じることもできます。

## <a name="example"></a>例

次の使用例は、 **BatchCollisionCount** プロパティと **Update** メソッドを使用して、バッチ更新を強制することで競合を解決するバッチ更新を示します。

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

