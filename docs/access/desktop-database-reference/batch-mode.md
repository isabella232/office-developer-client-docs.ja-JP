---
title: バッチ モード (デスクトップ データベース参照のアクセス)
TOCTitle: Batch Mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37f66f6ef6c4ed63b106584a6ac5118cddf20526
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861204"
---
# <a name="batch-mode"></a>バッチ モード


**適用されます**Access 2013 |。Office 2013

バッチ モードは、 **LockType** プロパティが **adLockBatchOptimistic** に設定されており、プロバイダーでバッチ更新がサポートされているときに有効になります。カーソル位置によっては、特定のロックの種類の設定が使用できない場合があります。たとえば、 **CursorLocation** が **adUseClient** に設定されているときは、排他的なロックを使用できません。反対に、カーソル位置がサーバー側にあるときは、プロバイダーがバッチ更新時の共有的ロックをサポートしていない場合があります。この場合、バッチ更新を実行できるのは、キーセット カーソルまたは静的カーソルのいずれかを使用する場合のみです。

**UpdateBatch** メソッドを使用すると、コピー バッファーに格納された **Recordset** の変更をサーバーに送信して、データ ソースを更新できます。次のセクションでは、 **Recordset** をバッチ モードで開き、コピー バッファーに変更を加えてから、 **UpdateBatch** を呼び出して変更をデータ ソースに送信します。

このセクションには、次のトピックが含まれています。

- [更新プログラムを送信する: UpdateBatch](sending-the-updates-updatebatch.md)

- [更新されたレコードにフィルターを適用する](filtering-for-updated-records.md)

- [失敗した更新操作に対処する](dealing-with-failed-updates.md)

- [競合を検出し、解決する](detecting-and-resolving-conflicts.md)

- [レコードセットを切断し、再接続する](disconnecting-and-reconnecting-the-recordset.md)

- [JOIN 操作の結果を更新する: Unique Table](updating-joined-results-unique-table.md)

