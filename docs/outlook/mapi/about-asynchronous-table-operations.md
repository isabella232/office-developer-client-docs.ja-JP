---
title: 非同期テーブルの操作について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 99bff153d4ce4bac3f85e0ed0feeaffafa6bf3f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799595"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="43c9e-103">非同期テーブルの操作について</span><span class="sxs-lookup"><span data-stu-id="43c9e-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="43c9e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="43c9e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="43c9e-105">**IMAPITable**インターフェイスには、非同期的に動作する 3 つのメソッドと非同期操作を制御するための 3 つの方法が含まれています。</span><span class="sxs-lookup"><span data-stu-id="43c9e-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="43c9e-106">次の表に、これらのメソッドを示します。</span><span class="sxs-lookup"><span data-stu-id="43c9e-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="43c9e-107">**非同期操作**</span><span class="sxs-lookup"><span data-stu-id="43c9e-107">**Asynchronous operation**</span></span>|<span data-ttu-id="43c9e-108">**非同期制御方式**</span><span class="sxs-lookup"><span data-stu-id="43c9e-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43c9e-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="43c9e-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="43c9e-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="43c9e-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="43c9e-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="43c9e-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="43c9e-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="43c9e-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="43c9e-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="43c9e-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="43c9e-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="43c9e-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="43c9e-115">**テーブルの種類と現在の操作に関するステータス情報を取得するには**</span><span class="sxs-lookup"><span data-stu-id="43c9e-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="43c9e-116">[IMAPITable::GetStatus](imapitable-getstatus.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="43c9e-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="43c9e-117">**GetStatus**とテーブルのユーザーがかどうか、テーブルは、静的または動的な場合は、操作が進行中または完了すると場合と、完了した操作から、エラーが発生したかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="43c9e-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="43c9e-118">などの場合は、クライアントでは、あまり時間がかかるために、並べ替え操作をキャンセルする必要がある、クライアント最初を呼び出せるかどうか、実際には、並べ替え操作は、現在の処理を決定するのには、 **GetStatus** 。</span><span class="sxs-lookup"><span data-stu-id="43c9e-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="43c9e-119">クライアントはそれを停止するのには[IMAPITable::Abort](imapitable-abort.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="43c9e-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="43c9e-120">**非同期タスクが完了するまで活動を中断するのには**</span><span class="sxs-lookup"><span data-stu-id="43c9e-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="43c9e-121">[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="43c9e-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="43c9e-122">**WaitForCompletion**を呼び出すことには、タスクを中断することがなく完了することができます。</span><span class="sxs-lookup"><span data-stu-id="43c9e-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="43c9e-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="43c9e-123">See also</span></span>

- [<span data-ttu-id="43c9e-124">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="43c9e-124">MAPI Tables</span></span>](mapi-tables.md)

