---
title: テーブルの通知について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3dfc67c8bcd899396da5371c614fd221cd9b2251
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799606"
---
# <a name="about-table-notifications"></a><span data-ttu-id="e149e-103">テーブルの通知について</span><span class="sxs-lookup"><span data-stu-id="e149e-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="e149e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e149e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e149e-105">クライアントは、多くの場合については、オブジェクトから直接通知を受け取るに登録する代わりにオブジェクトへの変更の通知をテーブルに依存しています。</span><span class="sxs-lookup"><span data-stu-id="e149e-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="e149e-106">通知の送信が発生する一般的な変更には、追加、削除、または行と、重大なエラーの修正が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e149e-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="e149e-107">通知が到着したとき、クライアントは、テーブルを再ロードするのには別の呼び出しを行うかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="e149e-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="e149e-108">テーブルの通知は非同期であるためより小さく単純な処理通知を行うことができるいくつかの問題があります。</span><span class="sxs-lookup"><span data-stu-id="e149e-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="e149e-109">[TABLE_NOTIFICATION](table_notification.md)構造体に渡されるデータは、テーブルの最新の状態を表さないことがあります。</span><span class="sxs-lookup"><span data-stu-id="e149e-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="e149e-110">たとえば、クライアントは、メッセージに変更を加えるし、それを削除します。</span><span class="sxs-lookup"><span data-stu-id="e149e-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="e149e-111">メッセージ ストア プロバイダーがメッセージに含まれているコンテンツのテーブルを実装する 2 つの通知を送信する: TABLE_ROW_MODIFIED のイベントの後に、TABLE_ROW_DELETED イベントです。</span><span class="sxs-lookup"><span data-stu-id="e149e-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="e149e-112">によってどのようにメッセージ ストア プロバイダーは、通知を時間、クライアントは、行の削除後 TABLE_ROW_MODIFIED 通知を受け取る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e149e-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="e149e-113">設定、通知に含まれる列は、テーブルの現在の列のセットとは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="e149e-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="e149e-114">MAPI では、通知の列のセットが、通知が生成された時点で有効であった列セットと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e149e-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="e149e-115">クライアントが任意の時点を設定する列を変更するのには[IMAPITable::SetColumns](imapitable-setcolumns.md)を呼び出すための可能性があるため-通知した場合を含め、2 つの列セットを同期できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e149e-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="e149e-116">ビューの一部である行のテーブルの通知を送信のみです。</span><span class="sxs-lookup"><span data-stu-id="e149e-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="e149e-117">制限があるため、ビューからの行が除外されている場合、またはテーブルが折りたたまれた状態であるため、通知が送信されますない場合はその行が変更されました。</span><span class="sxs-lookup"><span data-stu-id="e149e-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="e149e-118">また、カテゴリの状態の変更をクライアントに通知する通知は送信されません。</span><span class="sxs-lookup"><span data-stu-id="e149e-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="e149e-119">クライアントがありますしないすべてのテーブルが TABLE_SORT_DONE の通知をサポートしでこの条件を処理するために準備する必要。</span><span class="sxs-lookup"><span data-stu-id="e149e-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="e149e-120">同期する並べ替えを強制します。</span><span class="sxs-lookup"><span data-stu-id="e149e-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="e149e-121">[IMAPITable::SortTable](imapitable-sorttable.md)が返されるときに、テーブルの行を再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="e149e-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e149e-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="e149e-122">See also</span></span>



[<span data-ttu-id="e149e-123">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="e149e-123">MAPI Tables</span></span>](mapi-tables.md)

