---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 97575a65cd6825e07d6f11c813beec539f99f53a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436077"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="23257-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="23257-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="23257-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23257-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23257-105">カテゴリ化されたテーブルの現在の折りたたまれた状態または展開された状態を再構築するために必要なデータを返します。</span><span class="sxs-lookup"><span data-stu-id="23257-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="23257-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23257-106">Parameters</span></span>

 <span data-ttu-id="23257-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="23257-107">_ulFlags_</span></span>
  
> <span data-ttu-id="23257-108">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="23257-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="23257-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="23257-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="23257-110">順番_lpbInstanceKey_パラメーターによって示されるインスタンスキーのバイト数。</span><span class="sxs-lookup"><span data-stu-id="23257-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="23257-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="23257-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="23257-112">順番現在折りたたまれている状態または展開されている状態を再構築する必要がある行の**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="23257-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="23257-113">_lpbInstanceKey_パラメーターを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="23257-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="23257-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="23257-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="23257-115">読み上げ_lppbCollapseState_パラメーターによって参照されている構造体の数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="23257-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="23257-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="23257-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="23257-117">読み上げ現在のテーブルビューを説明するデータを含む構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="23257-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="23257-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="23257-118">Return value</span></span>

<span data-ttu-id="23257-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="23257-119">S_OK</span></span> 
  
> <span data-ttu-id="23257-120">カテゴリ内のテーブルの状態が正常に保存されました。</span><span class="sxs-lookup"><span data-stu-id="23257-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="23257-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="23257-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="23257-122">操作が開始されないように、別の操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="23257-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="23257-123">進行中の操作が完了することを許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23257-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="23257-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="23257-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="23257-125">このテーブルでは、分類と展開されたビューおよび折りたたまれたビューをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="23257-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="23257-126">注釈</span><span class="sxs-lookup"><span data-stu-id="23257-126">Remarks</span></span>

<span data-ttu-id="23257-127">**imapitable:: GetCollapseState**メソッドは[imapitable:: SetCollapseState](imapitable-setcollapsestate.md)メソッドを使用して、分類されたテーブルのユーザーのビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="23257-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="23257-128">**GetCollapseState**は、 **SetCollapseState**が、カテゴリに分類されたテーブルのカテゴリの適切なビューを再構築するために使用するために必要なデータを保存します。</span><span class="sxs-lookup"><span data-stu-id="23257-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="23257-129">サービスプロバイダーは、保存するデータを決定します。</span><span class="sxs-lookup"><span data-stu-id="23257-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="23257-130">ただし、 **GetCollapseState**を実装するほとんどのサービスプロバイダーでは、次の内容が保存されます。</span><span class="sxs-lookup"><span data-stu-id="23257-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="23257-131">並べ替えキー (標準列とカテゴリ列)。</span><span class="sxs-lookup"><span data-stu-id="23257-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="23257-132">インスタンスキーが表す行に関する情報。</span><span class="sxs-lookup"><span data-stu-id="23257-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="23257-133">表の折りたたまれたカテゴリと展開されたカテゴリを復元するための情報。</span><span class="sxs-lookup"><span data-stu-id="23257-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="23257-134">カテゴリ別テーブルの詳細については、「[並べ替えと分類](sorting-and-categorization.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23257-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="23257-135">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="23257-135">Notes to implementers</span></span>

<span data-ttu-id="23257-136">_lppbCollapseState_パラメーターに、テーブルのすべてのノードの現在の状態を格納します。</span><span class="sxs-lookup"><span data-stu-id="23257-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="23257-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="23257-137">Notes to callers</span></span>

<span data-ttu-id="23257-138">**SetCollapseState**を呼び出す前に、必ず**GetCollapseState**を呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="23257-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="23257-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="23257-139">See also</span></span>



[<span data-ttu-id="23257-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="23257-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="23257-141">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23257-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

