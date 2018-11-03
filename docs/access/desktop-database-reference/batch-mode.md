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
# <a name="batch-mode"></a><span data-ttu-id="c462f-102">バッチ モード</span><span class="sxs-lookup"><span data-stu-id="c462f-102">Batch mode</span></span>

<span data-ttu-id="c462f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c462f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c462f-p101">バッチ モードは、 **LockType** プロパティが **adLockBatchOptimistic** に設定されており、プロバイダーでバッチ更新がサポートされているときに有効になります。カーソル位置によっては、特定のロックの種類の設定が使用できない場合があります。たとえば、 **CursorLocation** が **adUseClient** に設定されているときは、排他的なロックを使用できません。反対に、カーソル位置がサーバー側にあるときは、プロバイダーがバッチ更新時の共有的ロックをサポートしていない場合があります。この場合、バッチ更新を実行できるのは、キーセット カーソルまたは静的カーソルのいずれかを使用する場合のみです。</span><span class="sxs-lookup"><span data-stu-id="c462f-p101">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider. Certain lock type settings are not available depending on cursor location. For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**. Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server. You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="c462f-p102">**UpdateBatch** メソッドを使用すると、コピー バッファーに格納された **Recordset** の変更をサーバーに送信して、データ ソースを更新できます。次のセクションでは、 **Recordset** をバッチ モードで開き、コピー バッファーに変更を加えてから、 **UpdateBatch** を呼び出して変更をデータ ソースに送信します。</span><span class="sxs-lookup"><span data-stu-id="c462f-p102">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source. In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

<span data-ttu-id="c462f-111">このセクションには、次のトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c462f-111">This section includes the following topics:</span></span>

- [<span data-ttu-id="c462f-112">更新を送信する: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="c462f-112">Sending the updates: UpdateBatch</span></span>](sending-the-updates-updatebatch.md)
- [<span data-ttu-id="c462f-113">更新されたレコードのフィルタ リング</span><span class="sxs-lookup"><span data-stu-id="c462f-113">Filtering for updated records</span></span>](filtering-for-updated-records.md)
- [<span data-ttu-id="c462f-114">失敗した更新を処理します。</span><span class="sxs-lookup"><span data-stu-id="c462f-114">Dealing with failed updates</span></span>](dealing-with-failed-updates.md)
- [<span data-ttu-id="c462f-115">検出して、競合を解決します。</span><span class="sxs-lookup"><span data-stu-id="c462f-115">Detecting and resolving conflicts</span></span>](detecting-and-resolving-conflicts.md)
- [<span data-ttu-id="c462f-116">接続を切断して、レコード セットを再接続します。</span><span class="sxs-lookup"><span data-stu-id="c462f-116">Disconnecting and reconnecting the Recordset</span></span>](disconnecting-and-reconnecting-the-recordset.md)
- [<span data-ttu-id="c462f-117">結合の結果を更新します固有のテーブル。</span><span class="sxs-lookup"><span data-stu-id="c462f-117">Updating JOINed results: Unique Table</span></span>](updating-joined-results-unique-table.md)

