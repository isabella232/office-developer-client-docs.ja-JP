---
title: 非同期テーブル操作について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: eebc04e2263b4a2037e167bd464a31d298b84664
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329021"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="07a8d-103">非同期テーブル操作について</span><span class="sxs-lookup"><span data-stu-id="07a8d-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="07a8d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07a8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07a8d-105">**IMAPITable**インターフェイスには、非同期操作を制御するための3つのメソッドを非同期で操作する3つのメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="07a8d-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="07a8d-106">次の表に、これらのメソッドを示します。</span><span class="sxs-lookup"><span data-stu-id="07a8d-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="07a8d-107">**非同期操作**</span><span class="sxs-lookup"><span data-stu-id="07a8d-107">**Asynchronous operation**</span></span>|<span data-ttu-id="07a8d-108">**非同期コントロールメソッド**</span><span class="sxs-lookup"><span data-stu-id="07a8d-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07a8d-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="07a8d-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="07a8d-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="07a8d-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="07a8d-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="07a8d-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="07a8d-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="07a8d-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="07a8d-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="07a8d-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="07a8d-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="07a8d-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="07a8d-115">**テーブルの種類と現在の操作に関する状態情報を取得するには**</span><span class="sxs-lookup"><span data-stu-id="07a8d-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="07a8d-116">呼び出し[IMAPITable:: GetStatus](imapitable-getstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="07a8d-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="07a8d-117">**GetStatus**では、テーブルのユーザーは、テーブルが静的または動的かどうか、操作が進行中であるか、完了したか、および完了した操作でエラーが発生したかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="07a8d-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="07a8d-118">たとえば、クライアントが時間がかかりすぎているために並べ替え操作を取り消す必要がある場合、最初に**GetStatus**を呼び出して、実際には並べ替え操作が現在処理中であるかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="07a8d-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="07a8d-119">その後、クライアントは[IMAPITable:: Abort](imapitable-abort.md)を呼び出して、これを停止できます。</span><span class="sxs-lookup"><span data-stu-id="07a8d-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="07a8d-120">**非同期タスクが完了するまでアクティビティを中断するには**</span><span class="sxs-lookup"><span data-stu-id="07a8d-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="07a8d-121">呼び出し[IMAPITable:: waitforcompletion](imapitable-waitforcompletion.md)。</span><span class="sxs-lookup"><span data-stu-id="07a8d-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="07a8d-122">**waitforcompletion**を呼び出すことにより、タスクを中断することなく完了できます。</span><span class="sxs-lookup"><span data-stu-id="07a8d-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="07a8d-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="07a8d-123">See also</span></span>

- [<span data-ttu-id="07a8d-124">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="07a8d-124">MAPI Tables</span></span>](mapi-tables.md)

