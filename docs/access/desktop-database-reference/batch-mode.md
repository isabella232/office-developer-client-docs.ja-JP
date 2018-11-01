---
title: バッチ モード (デスクトップ データベース参照のアクセス)
TOCTitle: Batch Mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ee4805f89d6a6a9d114c4347d808be61683efe6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880615"
---
# <a name="batch-mode"></a><span data-ttu-id="f824b-102">バッチ モード</span><span class="sxs-lookup"><span data-stu-id="f824b-102">Batch Mode</span></span>


<span data-ttu-id="f824b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f824b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f824b-p101">バッチ モードは、 **LockType** プロパティが **adLockBatchOptimistic** に設定されており、プロバイダーでバッチ更新がサポートされているときに有効になります。カーソル位置によっては、特定のロックの種類の設定が使用できない場合があります。たとえば、 **CursorLocation** が **adUseClient** に設定されているときは、排他的なロックを使用できません。反対に、カーソル位置がサーバー側にあるときは、プロバイダーがバッチ更新時の共有的ロックをサポートしていない場合があります。この場合、バッチ更新を実行できるのは、キーセット カーソルまたは静的カーソルのいずれかを使用する場合のみです。</span><span class="sxs-lookup"><span data-stu-id="f824b-p101">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider. Certain lock type settings are not available depending on cursor location. For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**. Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server. You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="f824b-p102">**UpdateBatch** メソッドを使用すると、コピー バッファーに格納された **Recordset** の変更をサーバーに送信して、データ ソースを更新できます。次のセクションでは、 **Recordset** をバッチ モードで開き、コピー バッファーに変更を加えてから、 **UpdateBatch** を呼び出して変更をデータ ソースに送信します。</span><span class="sxs-lookup"><span data-stu-id="f824b-p102">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source. In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

<span data-ttu-id="f824b-111">このセクションには、次のトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f824b-111">This section includes the following topics:</span></span>

- [<span data-ttu-id="f824b-112">更新プログラムを送信する: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="f824b-112">Sending the Updates: UpdateBatch</span></span>](sending-the-updates-updatebatch.md)

- [<span data-ttu-id="f824b-113">更新されたレコードにフィルターを適用する</span><span class="sxs-lookup"><span data-stu-id="f824b-113">Filtering for Updated Records</span></span>](filtering-for-updated-records.md)

- [<span data-ttu-id="f824b-114">失敗した更新操作に対処する</span><span class="sxs-lookup"><span data-stu-id="f824b-114">Dealing with Failed Updates</span></span>](dealing-with-failed-updates.md)

- [<span data-ttu-id="f824b-115">競合を検出し、解決する</span><span class="sxs-lookup"><span data-stu-id="f824b-115">Detecting and Resolving Conflicts</span></span>](detecting-and-resolving-conflicts.md)

- [<span data-ttu-id="f824b-116">レコードセットを切断し、再接続する</span><span class="sxs-lookup"><span data-stu-id="f824b-116">Disconnecting and Reconnecting the Recordset</span></span>](disconnecting-and-reconnecting-the-recordset.md)

- [<span data-ttu-id="f824b-117">JOIN 操作の結果を更新する: Unique Table</span><span class="sxs-lookup"><span data-stu-id="f824b-117">Updating JOINed Results: Unique Table</span></span>](updating-joined-results-unique-table.md)

