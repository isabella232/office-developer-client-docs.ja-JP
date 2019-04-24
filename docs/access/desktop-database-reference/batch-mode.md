---
title: バッチモード (Access デスクトップデータベースリファレンス)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac5f14d035a4e11cce67f01ca6636f3ebd39963e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296879"
---
# <a name="batch-mode"></a><span data-ttu-id="56689-102">バッチ モード</span><span class="sxs-lookup"><span data-stu-id="56689-102">Batch mode</span></span>

<span data-ttu-id="56689-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="56689-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56689-p101">バッチ モードは、 **LockType** プロパティが **adLockBatchOptimistic** に設定されており、プロバイダーでバッチ更新がサポートされているときに有効になります。カーソル位置によっては、特定のロックの種類の設定が使用できない場合があります。たとえば、 **CursorLocation** が **adUseClient** に設定されているときは、排他的なロックを使用できません。反対に、カーソル位置がサーバー側にあるときは、プロバイダーがバッチ更新時の共有的ロックをサポートしていない場合があります。この場合、バッチ更新を実行できるのは、キーセット カーソルまたは静的カーソルのいずれかを使用する場合のみです。</span><span class="sxs-lookup"><span data-stu-id="56689-p101">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider. Certain lock type settings are not available depending on cursor location. For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**. Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server. You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="56689-p102">**UpdateBatch** メソッドを使用すると、コピー バッファーに格納された **Recordset** の変更をサーバーに送信して、データ ソースを更新できます。次のセクションでは、 **Recordset** をバッチ モードで開き、コピー バッファーに変更を加えてから、 **UpdateBatch** を呼び出して変更をデータ ソースに送信します。</span><span class="sxs-lookup"><span data-stu-id="56689-p102">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source. In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

<span data-ttu-id="56689-111">このセクションでは、以下のトピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="56689-111">This section includes the following topics:</span></span>

- [<span data-ttu-id="56689-112">更新の送信: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="56689-112">Sending the updates: UpdateBatch</span></span>](sending-the-updates-updatebatch.md)
- [<span data-ttu-id="56689-113">更新済みのレコードのフィルター処理</span><span class="sxs-lookup"><span data-stu-id="56689-113">Filtering for updated records</span></span>](filtering-for-updated-records.md)
- [<span data-ttu-id="56689-114">失敗した更新の処理</span><span class="sxs-lookup"><span data-stu-id="56689-114">Dealing with failed updates</span></span>](dealing-with-failed-updates.md)
- [<span data-ttu-id="56689-115">競合の検出および解決</span><span class="sxs-lookup"><span data-stu-id="56689-115">Detecting and resolving conflicts</span></span>](detecting-and-resolving-conflicts.md)
- [<span data-ttu-id="56689-116">レコードセットの切断および再接続</span><span class="sxs-lookup"><span data-stu-id="56689-116">Disconnecting and reconnecting the Recordset</span></span>](disconnecting-and-reconnecting-the-recordset.md)
- [<span data-ttu-id="56689-117">JOINed の結果の更新: 固有のテーブル</span><span class="sxs-lookup"><span data-stu-id="56689-117">Updating JOINed results: Unique Table</span></span>](updating-joined-results-unique-table.md)

