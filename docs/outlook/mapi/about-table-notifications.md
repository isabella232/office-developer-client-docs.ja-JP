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
# <a name="about-table-notifications"></a><span data-ttu-id="a598d-103">テーブル通知について</span><span class="sxs-lookup"><span data-stu-id="a598d-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="a598d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a598d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a598d-105">クライアントは、オブジェクトから直接通知を受け取るように登録するのではなく、オブジェクトに対する変更を知るために table 通知に依存しています。</span><span class="sxs-lookup"><span data-stu-id="a598d-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="a598d-106">通知が送信される一般的な変更には、行の追加、削除、または変更、および重大なエラーがあります。</span><span class="sxs-lookup"><span data-stu-id="a598d-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="a598d-107">通知が到着すると、クライアントはテーブルを再読み込みするために別の呼び出しを行うかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="a598d-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="a598d-108">テーブル通知は非同期であるため、簡単な通知を処理できない問題がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="a598d-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="a598d-109">[TABLE_NOTIFICATION](table_notification.md)構造体で渡されるデータは、テーブルの最新の状態を表していない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a598d-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="a598d-110">たとえば、クライアントがメッセージに変更を加えた後、それを削除する場合があります。</span><span class="sxs-lookup"><span data-stu-id="a598d-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="a598d-111">メッセージを含むコンテンツテーブルを実装するメッセージストアプロバイダーは、2つの通知を送信します。 TABLE_ROW_MODIFIED イベントの後に TABLE_ROW_DELETED イベントが続きます。</span><span class="sxs-lookup"><span data-stu-id="a598d-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="a598d-112">メッセージストアプロバイダーの通知方法によっては、クライアントは行の削除後に TABLE_ROW_MODIFIED 通知を受け取ることがあります。</span><span class="sxs-lookup"><span data-stu-id="a598d-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="a598d-113">通知に含まれる列セットは、テーブルの現在の列セットと異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a598d-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="a598d-114">MAPI では、通知の列セットが通知が生成されたときに有効になっていた列セットと一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="a598d-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="a598d-115">クライアントは[IMAPITable:: SetColumns](imapitable-setcolumns.md)を呼び出すことができるので、いつでも列セットを変更することができます。これは、通知後に2つの列セットが同期されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a598d-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="a598d-116">テーブル通知は、ビューの一部である行に対してのみ送信されます。</span><span class="sxs-lookup"><span data-stu-id="a598d-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="a598d-117">つまり、制限によって、またはテーブルが折りたたまれた状態であるために、ある行がビューから除外されている場合、その行が変更されても通知は送信されません。</span><span class="sxs-lookup"><span data-stu-id="a598d-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="a598d-118">また、カテゴリ状態の変更についてクライアントに通知する通知は送信されません。</span><span class="sxs-lookup"><span data-stu-id="a598d-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="a598d-119">クライアントは、すべてのテーブルが TABLE_SORT_DONE 通知をサポートしているわけではなく、次のようにしてこの条件を処理できるようにする必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a598d-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="a598d-120">強制的に並べ替えを同期させます。</span><span class="sxs-lookup"><span data-stu-id="a598d-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="a598d-121">[IMAPITable:: sorttable](imapitable-sorttable.md)から返されるときに、テーブルの行を再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="a598d-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a598d-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="a598d-122">See also</span></span>



[<span data-ttu-id="a598d-123">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="a598d-123">MAPI Tables</span></span>](mapi-tables.md)

