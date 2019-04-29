---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 74c307fca27f1adec18d236792f8a58d97e33ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406151"
---
# <a name="imapitableabort"></a><span data-ttu-id="dc2ea-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="dc2ea-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="dc2ea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc2ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc2ea-105">テーブルに対して現在進行中のすべての非同期操作を停止します。</span><span class="sxs-lookup"><span data-stu-id="dc2ea-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="dc2ea-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dc2ea-106">Parameters</span></span>

<span data-ttu-id="dc2ea-107">なし</span><span class="sxs-lookup"><span data-stu-id="dc2ea-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="dc2ea-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="dc2ea-108">Return value</span></span>

<span data-ttu-id="dc2ea-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc2ea-109">S_OK</span></span> 
  
> <span data-ttu-id="dc2ea-110">1つ以上の非同期操作が停止されています。</span><span class="sxs-lookup"><span data-stu-id="dc2ea-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="dc2ea-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="dc2ea-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="dc2ea-112">非同期操作が進行中で、停止できないか、既に完了しています。</span><span class="sxs-lookup"><span data-stu-id="dc2ea-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc2ea-113">注釈</span><span class="sxs-lookup"><span data-stu-id="dc2ea-113">Remarks</span></span>

<span data-ttu-id="dc2ea-114">**IMAPITable:: Abort**メソッドは、現在進行中のすべての非同期操作を停止します。</span><span class="sxs-lookup"><span data-stu-id="dc2ea-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dc2ea-115">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="dc2ea-115">Notes to callers</span></span>

<span data-ttu-id="dc2ea-116">非同期操作が進行中かどうかを確認するには、 [IMAPITable:: GetStatus](imapitable-getstatus.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dc2ea-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="dc2ea-117">**中止**すると、 [IMAPITable:: Restrict](imapitable-restrict.md)メソッドへの呼び出しの処理が停止した場合、テーブルの状態は**abort**呼び出しが処理された時点の状態になります。</span><span class="sxs-lookup"><span data-stu-id="dc2ea-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="dc2ea-118">**中止**すると、 [IMAPITable:: sorttable](imapitable-sorttable.md)メソッドへの呼び出しの処理が停止した場合、テーブルの並べ替え順序は影響を受けず、 **sorttable**呼び出しの前と同じ状態になります。</span><span class="sxs-lookup"><span data-stu-id="dc2ea-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dc2ea-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc2ea-119">See also</span></span>



[<span data-ttu-id="dc2ea-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="dc2ea-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="dc2ea-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="dc2ea-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="dc2ea-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="dc2ea-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="dc2ea-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dc2ea-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

