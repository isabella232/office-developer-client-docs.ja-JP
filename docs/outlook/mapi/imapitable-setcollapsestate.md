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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328834"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="ad7f4-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ad7f4-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="ad7f4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad7f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad7f4-105">以前の[IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md)メソッドの呼び出しによって保存されたデータを使用して、カテゴリ化されたテーブルの現在の展開状態または折りたたみ状態を再構築します。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="ad7f4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ad7f4-106">Parameters</span></span>

 <span data-ttu-id="ad7f4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ad7f4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ad7f4-108">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ad7f4-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="ad7f4-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="ad7f4-110">順番_pbCollapseState_パラメーターによって参照されている構造体のバイト数。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="ad7f4-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="ad7f4-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="ad7f4-112">順番テーブルビューを再構築するために必要なデータを含む構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="ad7f4-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="ad7f4-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="ad7f4-114">読み上げ折りたたまれているか展開された状態を示す、テーブル内の行を識別するブックマークへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="ad7f4-115">このブックマークとインスタンスキーが[IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md)の呼び出しで_lpbInstanceKey_パラメーターに渡された場合、同じ行を識別します。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ad7f4-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="ad7f4-116">Return value</span></span>

<span data-ttu-id="ad7f4-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad7f4-117">S_OK</span></span> 
  
> <span data-ttu-id="ad7f4-118">カテゴリ化されたテーブルの状態が正常に再構築されました。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="ad7f4-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="ad7f4-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="ad7f4-120">操作が開始されないように、別の操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="ad7f4-121">進行中の操作が完了することを許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="ad7f4-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="ad7f4-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="ad7f4-123">テーブルで、折りたたまれたビューまたは展開されたビューの再構築を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad7f4-124">解説</span><span class="sxs-lookup"><span data-stu-id="ad7f4-124">Remarks</span></span>

<span data-ttu-id="ad7f4-125">**IMAPITable:: SetCollapseState**メソッドは、テーブルビューの展開または折りたたみ状態を再度確立します。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="ad7f4-126">**SetCollapseState**と**GetCollapseState**は、次のように連携して動作します。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="ad7f4-127">カテゴリ内のテーブルの状態が変更されるときに、 [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md)が呼び出され、変更前の状態に関するすべてのデータが保存されます。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="ad7f4-128">テーブルのビューを保存された状態に復元するには、 **SetCollapseState**が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="ad7f4-129">**GetCollapseState**によって保存されたデータは、 **SetCollapseState**に渡されます。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="ad7f4-130">**SetCollapseState**は、そのデータを使用して状態を復元できます。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="ad7f4-131">**SetCollapseState**は、 **GetCollapseState**への入力として渡されたインスタンスキーと同じ行を識別するブックマークを出力パラメーターとして返します。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="ad7f4-132">カテゴリ別テーブルの詳細については、「[並べ替えと分類](sorting-and-categorization.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ad7f4-133">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="ad7f4-133">Notes to implementers</span></span>

<span data-ttu-id="ad7f4-134">並べ替えの順序と制限が**GetCollapseState**呼び出し時とまったく同じであることを確認する責任があります。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="ad7f4-135">変更が行われた場合、結果は予測できないため、 **SetCollapseState**を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="ad7f4-136">これは、たとえば、クライアントが**GetCollapseState**を呼び出してから、 **SetCollapseState**を呼び出す前に並べ替えキーを変更するために、 **sorttable**を呼び出した場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="ad7f4-137">安全にするには、復元を続行する前に、保存したデータが有効であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ad7f4-138">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ad7f4-138">Notes to callers</span></span>

<span data-ttu-id="ad7f4-139">**SetCollapseState**を呼び出すには、以前に**GetCollapseState**と呼ばれていなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="ad7f4-140">カテゴリを確立する並べ替え順序は、両方の方法で同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="ad7f4-141">並べ替え順序が異なる場合、 **SetCollapseState**操作の結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="ad7f4-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ad7f4-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad7f4-142">See also</span></span>



[<span data-ttu-id="ad7f4-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="ad7f4-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="ad7f4-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="ad7f4-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="ad7f4-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ad7f4-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="ad7f4-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ad7f4-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

