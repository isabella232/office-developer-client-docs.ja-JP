---
title: バッチ モード (Access デスクトップ データベースリファレンス)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5913407ab7071d2f6664a1a22d60911a63479231
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558850"
---
# <a name="batch-mode"></a>バッチ モード

**適用先:** Access 2013、Office 2013

バッチ モードは、 **LockType** プロパティが **adLockBatchOptimistic** に設定されており、プロバイダーでバッチ更新がサポートされているときに有効になります。カーソル位置によっては、特定のロックの種類の設定が使用できない場合があります。たとえば、 **CursorLocation** が **adUseClient** に設定されているときは、排他的なロックを使用できません。反対に、カーソル位置がサーバー側にあるときは、プロバイダーがバッチ更新時の共有的ロックをサポートしていない場合があります。この場合、バッチ更新を実行できるのは、キーセット カーソルまたは静的カーソルのいずれかを使用する場合のみです。

**UpdateBatch** メソッドを使用すると、コピー バッファーに格納された **Recordset** の変更をサーバーに送信して、データ ソースを更新できます。次のセクションでは、 **Recordset** をバッチ モードで開き、コピー バッファーに変更を加えてから、 **UpdateBatch** を呼び出して変更をデータ ソースに送信します。

このセクションでは、以下のトピックについて説明します。

- [更新の送信: UpdateBatch](sending-the-updates-updatebatch.md)
- [更新済みのレコードのフィルター処理](filtering-for-updated-records.md)
- [失敗した更新の処理](dealing-with-failed-updates.md)
- [競合の検出および解決](detecting-and-resolving-conflicts.md)
- [レコードセットの切断および再接続](disconnecting-and-reconnecting-the-recordset.md)
- [JOINed の結果の更新: 固有のテーブル](updating-joined-results-unique-table.md)

