---
title: バッチ モード (デスクトップ データベース参照のアクセス)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9541e8b7888f5fb5f16bcfb343d545cf304b1afd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945790"
---
# <a name="batch-mode"></a>バッチ モード

**適用されます**Access 2013、Office 2013。

バッチ モードは、 **LockType** プロパティが **adLockBatchOptimistic** に設定されており、プロバイダーでバッチ更新がサポートされているときに有効になります。カーソル位置によっては、特定のロックの種類の設定が使用できない場合があります。たとえば、 **CursorLocation** が **adUseClient** に設定されているときは、排他的なロックを使用できません。反対に、カーソル位置がサーバー側にあるときは、プロバイダーがバッチ更新時の共有的ロックをサポートしていない場合があります。この場合、バッチ更新を実行できるのは、キーセット カーソルまたは静的カーソルのいずれかを使用する場合のみです。

**UpdateBatch** メソッドを使用すると、コピー バッファーに格納された **Recordset** の変更をサーバーに送信して、データ ソースを更新できます。次のセクションでは、 **Recordset** をバッチ モードで開き、コピー バッファーに変更を加えてから、 **UpdateBatch** を呼び出して変更をデータ ソースに送信します。

このセクションには、次のトピックが含まれています。

- [更新を送信する: UpdateBatch](sending-the-updates-updatebatch.md)
- [更新されたレコードのフィルタ リング](filtering-for-updated-records.md)
- [失敗した更新を処理します。](dealing-with-failed-updates.md)
- [検出して、競合を解決します。](detecting-and-resolving-conflicts.md)
- [接続を切断して、レコード セットを再接続します。](disconnecting-and-reconnecting-the-recordset.md)
- [結合の結果を更新します固有のテーブル。](updating-joined-results-unique-table.md)

