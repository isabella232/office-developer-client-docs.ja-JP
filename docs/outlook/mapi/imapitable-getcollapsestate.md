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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2c1246c46e9723cd3f6d92f0a44fc1419eef4a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800829"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="7b9c7-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="7b9c7-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="7b9c7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b9c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b9c7-105">現在を再構築するために必要なデータを返しますは、折りたたむか、カテゴリ別のテーブルの状態を展開します。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="7b9c7-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="7b9c7-106">Parameters</span></span>

 <span data-ttu-id="7b9c7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7b9c7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7b9c7-108">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7b9c7-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="7b9c7-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="7b9c7-110">[in]_LpbInstanceKey_パラメーターが指すインスタンスのキーのバイト数です。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="7b9c7-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="7b9c7-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="7b9c7-112">[in]現在の折りたたみまたは展開された状態の行の**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) のプロパティへのポインターを再構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="7b9c7-113">_LpbInstanceKey_パラメーターは、NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="7b9c7-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="7b9c7-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="7b9c7-115">[out]_LppbCollapseState_パラメーターが指す構造体の数へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="7b9c7-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="7b9c7-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="7b9c7-117">[out]現在のテーブル ビューを記述するデータを含む構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7b9c7-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="7b9c7-118">Return value</span></span>

<span data-ttu-id="7b9c7-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b9c7-119">S_OK</span></span> 
  
> <span data-ttu-id="7b9c7-120">分類されたテーブルの状態が正常に保存されました。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="7b9c7-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="7b9c7-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="7b9c7-122">別の操作は、操作の開始を防止する処理中です。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="7b9c7-123">実行中の操作を完了できるか、それを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="7b9c7-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7b9c7-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7b9c7-125">テーブルは、分類し、展開と縮小のビューをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b9c7-126">備考</span><span class="sxs-lookup"><span data-stu-id="7b9c7-126">Remarks</span></span>

<span data-ttu-id="7b9c7-127">**IMAPITable::GetCollapseState**メソッドは、ユーザーの分類されたテーブルのビューを変更するのには[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)メソッドを使用して動作します。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="7b9c7-128">**GetCollapseState**は、 **SetCollapseState**を使用して適切なカテゴリに分類されたテーブルのビューを再構築するのに必要なデータを保存します。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="7b9c7-129">サービス プロバイダーは、保存するデータを決定します。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="7b9c7-130">ただし、 **GetCollapseState**を実装するほとんどのサービス プロバイダーは、次を保存します。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="7b9c7-131">(標準の列と列のカテゴリ) の並べ替えのキーです。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="7b9c7-132">インスタンス キーを表す行に関する情報です。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="7b9c7-133">テーブルの折りたたみと展開されているカテゴリを復元する情報です。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="7b9c7-134">分類されたテーブルの詳細については、[並べ替えや分類](sorting-and-categorization.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7b9c7-135">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="7b9c7-135">Notes to implementers</span></span>

<span data-ttu-id="7b9c7-136">_LppbCollapseState_パラメーターでは、テーブルのすべてのノードの現在の状態を格納します。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7b9c7-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7b9c7-137">Notes to callers</span></span>

<span data-ttu-id="7b9c7-138">常に**SetCollapseState**を呼び出す前に**GetCollapseState**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7b9c7-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7b9c7-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="7b9c7-139">See also</span></span>



[<span data-ttu-id="7b9c7-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="7b9c7-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="7b9c7-141">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b9c7-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

