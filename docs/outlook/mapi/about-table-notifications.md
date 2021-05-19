---
title: テーブル通知について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9a42ed1e196e8ac498ab5889b4419ff407db4748
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417953"
---
# <a name="about-table-notifications"></a><span data-ttu-id="bb5e1-103">テーブル通知について</span><span class="sxs-lookup"><span data-stu-id="bb5e1-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="bb5e1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb5e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb5e1-105">クライアントは、多くの場合、オブジェクトから直接通知を受信するために登録する代わりに、テーブル通知を使用してオブジェクトに対する変更を学習します。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="bb5e1-106">通知の送信を引き起こす一般的な変更には、行の追加、削除、または変更、重大なエラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="bb5e1-107">通知が到着すると、クライアントはテーブルを再読み込みするために別の呼び出しを行うかどうかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="bb5e1-108">テーブル通知は非同期なので、通知の処理を簡単に行う可能性があるいくつかの問題があります。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="bb5e1-109">TABLE_NOTIFICATION構造で [渡されたデータ](table_notification.md) は、テーブルの最新の状態を表していない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="bb5e1-110">たとえば、クライアントがメッセージに変更を行い、メッセージを削除する場合があります。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="bb5e1-111">メッセージを含むコンテンツ テーブルを実装するメッセージ ストア プロバイダーは、TABLE_ROW_MODIFIED イベントとイベントの 2 つの通知TABLE_ROW_DELETEDします。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="bb5e1-112">メッセージ ストア プロバイダーが通知を回す方法に応じて、クライアントは行の削除後にTABLE_ROW_MODIFIED通知を受け取る場合があります。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="bb5e1-113">通知に含まれる列セットは、テーブルの現在の列セットとは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="bb5e1-114">MAPI では、通知列セットが、通知が生成された時点で有効だった列セットと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="bb5e1-115">クライアントが [IMAPITable::SetColumns](imapitable-setcolumns.md) を呼び出して、通知後も含めていつでも列セットを変更できる可能性があるから、2 つの列セットは同期できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="bb5e1-116">テーブル通知は、ビューの一部である行にのみ送信されます。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="bb5e1-117">つまり、制限のために行がビューから除外されている場合、またはテーブルが折りたたみ状態にある場合、その行が変更された場合は通知は送信されません。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="bb5e1-118">また、カテゴリの状態の変更についてクライアントに通知する通知は送信されません。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="bb5e1-119">クライアントは、すべてのテーブルが通知をサポートしているTABLE_SORT_DONE、次の方法でこの条件を処理する準備が必要です。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="bb5e1-120">並べ替えを同期に設定します。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="bb5e1-121">[IMAPITable::SortTable が返された場合にテーブルの行を](imapitable-sorttable.md)再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="bb5e1-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="bb5e1-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb5e1-122">See also</span></span>



[<span data-ttu-id="bb5e1-123">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="bb5e1-123">MAPI Tables</span></span>](mapi-tables.md)

