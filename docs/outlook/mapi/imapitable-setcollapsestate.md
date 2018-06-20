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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 252b6d6c7ff74acd5f0b288af48ff2901c2330ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800864"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="ce741-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ce741-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="ce741-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce741-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ce741-105">[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)メソッドへの前回の呼び出しによって保存されたデータを使用して分類されたテーブルの現在の展開または折りたたみの状態を再構築します。</span><span class="sxs-lookup"><span data-stu-id="ce741-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="ce741-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="ce741-106">Parameters</span></span>

 <span data-ttu-id="ce741-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ce741-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ce741-108">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce741-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ce741-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="ce741-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="ce741-110">[in]_PbCollapseState_パラメーターが指す構造体のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="ce741-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="ce741-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="ce741-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="ce741-112">[in]テーブル ビューを再構築するために必要なデータを含む構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ce741-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="ce741-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="ce741-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="ce741-114">[out]折りたたまれた状態または展開された状態の再構築するテーブル内の行を識別するブックマークへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ce741-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="ce741-115">このブックマークと[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)への呼び出し内の_lpbInstanceKey_パラメーターで渡されるインスタンスのキーは、同じ行を識別します。</span><span class="sxs-lookup"><span data-stu-id="ce741-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ce741-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ce741-116">Return value</span></span>

<span data-ttu-id="ce741-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce741-117">S_OK</span></span> 
  
> <span data-ttu-id="ce741-118">分類されたテーブルの状態が正常に再構築されました。</span><span class="sxs-lookup"><span data-stu-id="ce741-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="ce741-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="ce741-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="ce741-120">別の操作は、操作の開始を防止する処理中です。</span><span class="sxs-lookup"><span data-stu-id="ce741-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="ce741-121">実行中の操作を完了できるか、それを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce741-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="ce741-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="ce741-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="ce741-123">テーブルでは、折りたたまれた状態または展開されたビューの再構築が完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="ce741-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce741-124">備考</span><span class="sxs-lookup"><span data-stu-id="ce741-124">Remarks</span></span>

<span data-ttu-id="ce741-125">**IMAPITable::SetCollapseState**メソッドは、テーブル ビューの展開または折りたたみの状態を再確立します。</span><span class="sxs-lookup"><span data-stu-id="ce741-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="ce741-126">**SetCollapseState**および**GetCollapseState**が次のように協力しています。</span><span class="sxs-lookup"><span data-stu-id="ce741-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="ce741-127">分類されたテーブルの状態を変更しようとしていますが、すべての変更前の状態に関連するデータを保存するのには[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ce741-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="ce741-128">テーブルのビューを保存した状態に復元するに**SetCollapseState**が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ce741-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="ce741-129">**GetCollapseState**によって保存されたデータは、 **SetCollapseState**に渡されます。</span><span class="sxs-lookup"><span data-stu-id="ce741-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="ce741-130">**SetCollapseState**は、状態を復元するのにはそのデータを使用することです。</span><span class="sxs-lookup"><span data-stu-id="ce741-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="ce741-131">**SetCollapseState**は、出力パラメーターとして**GetCollapseState**への入力として渡されるインスタンスのキーとして同じ行を識別するブックマークを返します。</span><span class="sxs-lookup"><span data-stu-id="ce741-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="ce741-132">分類されたテーブルの詳細については、[並べ替えや分類](sorting-and-categorization.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce741-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ce741-133">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="ce741-133">Notes to implementers</span></span>

<span data-ttu-id="ce741-134">並べ替え順序および制限、正確に同じである**GetCollapseState**の呼び出しの時と同様に確認する責任があります。</span><span class="sxs-lookup"><span data-stu-id="ce741-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="ce741-135">変更を行った結果を予測できるので**SetCollapseState**は呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="ce741-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="ce741-136">**GetCollapseState**とし、 **SortTable** **SetCollapseState**を呼び出す前に、並べ替えのキーを変更するのなど、クライアントが呼び出す場合は、これが起こります。</span><span class="sxs-lookup"><span data-stu-id="ce741-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="ce741-137">安全のため、保存されたデータは復元を続行する前に有効なことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ce741-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ce741-138">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ce741-138">Notes to callers</span></span>

<span data-ttu-id="ce741-139">**SetCollapseState**を呼び出すには、する必要がありますが以前と呼ばれる**GetCollapseState**。</span><span class="sxs-lookup"><span data-stu-id="ce741-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="ce741-140">カテゴリを確立する並べ替え順序は、どちらのメソッドも同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce741-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="ce741-141">並べ替え順が異なる場合、 **SetCollapseState**操作の結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="ce741-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ce741-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="ce741-142">See also</span></span>



[<span data-ttu-id="ce741-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="ce741-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="ce741-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="ce741-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="ce741-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ce741-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="ce741-146">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce741-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

