---
title: Recordset2.BatchSize プロパティ (DAO)
TOCTitle: BatchSize Property
ms:assetid: fa7f12f6-36c8-5aad-31d2-668cfe46f9f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837054(v=office.15)
ms:contentKeyID: 48548846
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edb0f18e68021bf6e23e006d5d8e37e6eb6d816c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867952"
---
# <a name="recordset2batchsize-property-dao"></a>Recordset2.BatchSize プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

## <a name="syntax"></a>構文

*式*です。BatchSize

*式***Recordset2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**BatchSize** プロパティは、バッチ更新でステートメントをサーバーに送信するときに使用されるバッチ サイズを決定します。このプロパティの値は、1 つのコマンド バッファーでサーバーに送信されるステートメントの数を決定します。既定では、各バッチで 15 個のステートメントがサーバーに送信されます。このプロパティはいつでも変更できます。データベース サーバーがステートメントのバッチ処理をサポートしていない場合、このプロパティを 1 に設定すると、各ステートメントが個別に送信されます。

## <a name="example"></a>例

次の使用例は、 **BatchSize** プロパティおよび **UpdateOptions** プロパティを使用して、指定した Recordset オブジェクトの任意のバッチ更新の環境を制御します。

```vb
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
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
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

