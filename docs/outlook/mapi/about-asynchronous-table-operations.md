---
title: 非同期テーブルの操作について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1c31045e1fc19da63a2d4b61d92b3629afc96a55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569422"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="e3a3c-103">非同期テーブルの操作について</span><span class="sxs-lookup"><span data-stu-id="e3a3c-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="e3a3c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3a3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3a3c-105">**IMAPITable**インターフェイスには、非同期的に動作する 3 つのメソッドと非同期操作を制御するための 3 つの方法が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e3a3c-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="e3a3c-106">次の表に、これらのメソッドを示します。</span><span class="sxs-lookup"><span data-stu-id="e3a3c-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="e3a3c-107">**非同期操作**</span><span class="sxs-lookup"><span data-stu-id="e3a3c-107">**Asynchronous operation**</span></span>|<span data-ttu-id="e3a3c-108">**非同期制御方式**</span><span class="sxs-lookup"><span data-stu-id="e3a3c-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3a3c-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="e3a3c-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="e3a3c-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="e3a3c-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="e3a3c-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="e3a3c-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="e3a3c-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="e3a3c-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="e3a3c-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="e3a3c-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="e3a3c-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e3a3c-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="e3a3c-115">**テーブルの種類と現在の操作に関するステータス情報を取得するには**</span><span class="sxs-lookup"><span data-stu-id="e3a3c-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="e3a3c-116">[IMAPITable::GetStatus](imapitable-getstatus.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e3a3c-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="e3a3c-117">**GetStatus**とテーブルのユーザーがかどうか、テーブルは、静的または動的な場合は、操作が進行中または完了すると場合と、完了した操作から、エラーが発生したかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="e3a3c-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="e3a3c-118">などの場合は、クライアントでは、あまり時間がかかるために、並べ替え操作をキャンセルする必要がある、クライアント最初を呼び出せるかどうか、実際には、並べ替え操作は、現在の処理を決定するのには、 **GetStatus** 。</span><span class="sxs-lookup"><span data-stu-id="e3a3c-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="e3a3c-119">クライアントはそれを停止するのには[IMAPITable::Abort](imapitable-abort.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="e3a3c-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="e3a3c-120">**非同期タスクが完了するまで活動を中断するのには**</span><span class="sxs-lookup"><span data-stu-id="e3a3c-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="e3a3c-121">[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e3a3c-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="e3a3c-122">**WaitForCompletion**を呼び出すことには、タスクを中断することがなく完了することができます。</span><span class="sxs-lookup"><span data-stu-id="e3a3c-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e3a3c-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3a3c-123">See also</span></span>

- [<span data-ttu-id="e3a3c-124">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="e3a3c-124">MAPI Tables</span></span>](mapi-tables.md)

