---
title: IMAPITableSetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetCollapseState
api_type:
- COM
ms.assetid: 31325e8f-1cf9-49b2-8118-953996b0037f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7351457dc5b72cfc4a7ef9f91e9d33a80ca98c39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414068"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="1f55a-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="1f55a-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="1f55a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f55a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f55a-105">[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)メソッドの以前の呼び出しによって保存されたデータを使用して、分類されたテーブルの現在の展開状態または折りたたみ状態を再構築します。</span><span class="sxs-lookup"><span data-stu-id="1f55a-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="1f55a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1f55a-106">Parameters</span></span>

 <span data-ttu-id="1f55a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1f55a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1f55a-108">予約済み。は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f55a-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1f55a-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="1f55a-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="1f55a-110">[in]  _pbCollapseState_ パラメーターが指す構造体内のバイト数。</span><span class="sxs-lookup"><span data-stu-id="1f55a-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="1f55a-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="1f55a-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="1f55a-112">[in]テーブル ビューの再構築に必要なデータを含む構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1f55a-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="1f55a-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="1f55a-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="1f55a-114">[out]折りたたみまたは展開された状態を再構築するテーブル内の行を識別するブックマークへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1f55a-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="1f55a-115">[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)への呼び出しで _lpbInstanceKey_ パラメーターに渡されたこのブックマークとインスタンス キーは、同じ行を識別します。</span><span class="sxs-lookup"><span data-stu-id="1f55a-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1f55a-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="1f55a-116">Return value</span></span>

<span data-ttu-id="1f55a-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="1f55a-117">S_OK</span></span> 
  
> <span data-ttu-id="1f55a-118">分類されたテーブルの状態が正常に再構築されました。</span><span class="sxs-lookup"><span data-stu-id="1f55a-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="1f55a-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="1f55a-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="1f55a-120">操作の開始を妨げる別の操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="1f55a-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="1f55a-121">進行中の操作の完了を許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f55a-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="1f55a-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="1f55a-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="1f55a-123">テーブルが折りたたみビューまたは展開ビューの再構築を終了する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="1f55a-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f55a-124">注釈</span><span class="sxs-lookup"><span data-stu-id="1f55a-124">Remarks</span></span>

<span data-ttu-id="1f55a-125">**IMAPITable::SetCollapseState** メソッドは、テーブル ビューの展開または折りたたみ状態を再確立します。</span><span class="sxs-lookup"><span data-stu-id="1f55a-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="1f55a-126">**SetCollapseState と** **GetCollapseState は、** 次のように一緒に動作します。</span><span class="sxs-lookup"><span data-stu-id="1f55a-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="1f55a-127">分類されたテーブルの状態が変更され始め [、IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) が呼び出され、変更前の状態に関連するデータをすべて保存します。</span><span class="sxs-lookup"><span data-stu-id="1f55a-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="1f55a-128">テーブルのビューを保存された状態に復元するには **、SetCollapseState が** 呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1f55a-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="1f55a-129">**GetCollapseState によって保存されたデータは** **SetCollapseState に渡されます**。</span><span class="sxs-lookup"><span data-stu-id="1f55a-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="1f55a-130">**SetCollapseState** は、そのデータを使用して状態を復元できます。</span><span class="sxs-lookup"><span data-stu-id="1f55a-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="1f55a-131">**SetCollapseState** は **、GetCollapseState** に入力として渡されたインスタンス キーと同じ行を識別するブックマークを出力パラメーターとして返します。</span><span class="sxs-lookup"><span data-stu-id="1f55a-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="1f55a-132">分類テーブルの詳細については、「並べ替えと [分類」を参照してください](sorting-and-categorization.md)。</span><span class="sxs-lookup"><span data-stu-id="1f55a-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1f55a-133">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="1f55a-133">Notes to implementers</span></span>

<span data-ttu-id="1f55a-134">並べ替え順序と制限が **GetCollapseState** 呼び出し時とまったく同じことを確認する責任があります。</span><span class="sxs-lookup"><span data-stu-id="1f55a-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="1f55a-135">変更が行われた場合、結果が予測できない可能性があるため **、SetCollapseState** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f55a-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="1f55a-136">これは、たとえば、クライアントが **GetCollapseState** を呼び出してから **SortTable** を呼び出して **、SetCollapseState** を呼び出す前に並べ替えキーを変更する場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="1f55a-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="1f55a-137">安全を確保するには、復元を進む前に、保存されたデータがまだ有効か確認してください。</span><span class="sxs-lookup"><span data-stu-id="1f55a-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1f55a-138">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="1f55a-138">Notes to callers</span></span>

<span data-ttu-id="1f55a-139">**SetCollapseState** を呼び出す場合は、**以前に GetCollapseState** を呼び出している必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f55a-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="1f55a-140">カテゴリを確立する並べ替え順序は、両方のメソッドで同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f55a-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="1f55a-141">並べ替え順序が異なる場合 **、SetCollapseState** 操作の結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="1f55a-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f55a-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="1f55a-142">See also</span></span>



[<span data-ttu-id="1f55a-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="1f55a-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="1f55a-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="1f55a-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="1f55a-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="1f55a-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="1f55a-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f55a-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

