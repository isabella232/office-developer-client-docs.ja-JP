---
title: Recordset.UpdateOptions プロパティ (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 14ab955d-1c5a-dc76-8dbf-dbca49816bc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845468(v=office.15)
ms:contentKeyID: 48543391
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101185
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: b4237ac6062a69d9a649d988015e75424b1d1c7d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617553"
---
# <a name="recordsetupdateoptions-property-dao"></a>Recordset.UpdateOptions プロパティ (DAO)


**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式* .UpdateOptions

*式* **Recordset** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

バッチモードの **[Update](recordset-update-method-dao.md)** を実行すると、DAO とクライアント バッチ カーソル ライブラリによって必要な変更を行う一連の SQL UPDATE ステートメントが作成されます。 更新ごとに、 **[RecordStatus](recordset-recordstatus-property-dao.md)** プロパティによって変更済みのマークが付けられたレコードを分離する SQL WHERE 句が作成されます。 一部のリモート サーバーではトリガーやその他の方法を使用して参照整合性を強制しているため、多くの場合、更新対象のフィールドを変更の影響を受けるフィールドのみに制限することが重要です。 

そのためには、 **UpdateOptions** プロパティを **dbCriteriaKey**、 **dbCriteriaModValues**、 **dbCriteriaAllCols**、 **dbCriteriaTimeStamp** のいずれかの定数に設定します。 こうすると、必要最低限のトリガー コードが実行されます。 結果として、更新操作が速くなり、エラーの可能性も少なくなります。

また、 **dbCriteriaDeleteInsert** 定数または **dbCriteriaUpdate** 定数を連結すると、バッチ変更をサーバーに返信する際に、各更新に対して SQL DELETE ステートメントと INSERT ステートメントのセット、または SQL UPDATE ステートメントを使用するかどうかを指定できます。前者の場合、レコードの更新には、2 つの異なる操作が必要となります。正しい **UpdateOptions** プロパティの設定を選択すると、パフォーマンスを大幅に向上させることができる場合があります (特にリモート システムに DELETE、INSERT、および UPDATE の各トリガーが実装されている場合)。

定数を指定しない場合、 **dbCriteriaUpdate** および **dbCriteriaKey** が使用されます。

新規レコードの追加では、常に INSERT ステートメントが生成され、レコードの削除では、常に DELETE ステートメントが生成されるため、このプロパティは、カーソル ライブラリによる変更レコードの更新の方法にのみ適用されます。

## <a name="example"></a>例

次の例では、 **BatchSize** プロパティおよび **UpdateOptions** プロパティを使用して、指定された **Recordset** オブジェクトに対するバッチ更新の諸条件を制御します。

```vb 
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
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

