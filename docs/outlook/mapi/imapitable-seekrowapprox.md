---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 12b0c9b40c7ff06e9a3cf8e7929489f30434fa12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800863"
---
# <a name="imapitableseekrowapprox"></a><span data-ttu-id="e1563-103">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="e1563-103">IMAPITable::SeekRowApprox</span></span>

  
  
<span data-ttu-id="e1563-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e1563-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e1563-105">テーブルのおおよその小数部から成る位置にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="e1563-105">Moves the cursor to an approximate fractional position in the table.</span></span> 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="e1563-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e1563-106">Parameters</span></span>

 <span data-ttu-id="e1563-107">_ulNumerator_</span><span class="sxs-lookup"><span data-stu-id="e1563-107">_ulNumerator_</span></span>
  
> <span data-ttu-id="e1563-108">[in]テーブルの位置を表す分数の分子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e1563-108">[in] Pointer to the numerator of the fraction representing the table position.</span></span> <span data-ttu-id="e1563-109">_UlNumerator_パラメーターが 0 の場合は、分母の値に関係なく、テーブルの先頭にカーソルが配置されます。</span><span class="sxs-lookup"><span data-stu-id="e1563-109">If the  _ulNumerator_ parameter is zero, the cursor is positioned at the beginning of the table regardless of the denominator value.</span></span> <span data-ttu-id="e1563-110">_UlNumerator_が_ulDenominator_のパラメーターと等しい場合は、カーソルはテーブルの最後の行の後です。</span><span class="sxs-lookup"><span data-stu-id="e1563-110">If  _ulNumerator_ is equal to the  _ulDenominator_ parameter, the cursor is positioned after the last table row.</span></span> 
    
 <span data-ttu-id="e1563-111">_ulDenominator_</span><span class="sxs-lookup"><span data-stu-id="e1563-111">_ulDenominator_</span></span>
  
> <span data-ttu-id="e1563-112">[in]テーブルの位置を表す分数の分母となるへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e1563-112">[in] Pointer to the denominator of the fraction representing the table position.</span></span> <span data-ttu-id="e1563-113">_UlDenominator_パラメーターは、ゼロにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e1563-113">The  _ulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e1563-114">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e1563-114">Return value</span></span>

<span data-ttu-id="e1563-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="e1563-115">S_OK</span></span> 
  
> <span data-ttu-id="e1563-116">シーク操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="e1563-116">The seek operation was successful.</span></span>
    
<span data-ttu-id="e1563-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="e1563-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="e1563-118">別の操作は、シーク操作の開始行を防止する処理中です。</span><span class="sxs-lookup"><span data-stu-id="e1563-118">Another operation is in progress that prevents the row seeking operation from starting.</span></span> <span data-ttu-id="e1563-119">実行中の操作を完了できるか、それを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1563-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1563-120">注釈</span><span class="sxs-lookup"><span data-stu-id="e1563-120">Remarks</span></span>

<span data-ttu-id="e1563-121">**IMAPITable::SeekRowApprox**メソッドを呼び出した後、テーブルのカーソル位置は、ヒューリスティックによって、正確なことができない場合があります分数です。</span><span class="sxs-lookup"><span data-stu-id="e1563-121">The cursor position in a table after a call to the **IMAPITable::SeekRowApprox** method is heuristically the fraction and might not be exact.</span></span> <span data-ttu-id="e1563-122">たとえば、特定のプロバイダーを実装バイナリ ツリーは、上にテーブル パフォーマンス上の理由から、ツリーの最上部にテーブルの中間点を扱うこと。</span><span class="sxs-lookup"><span data-stu-id="e1563-122">For example, certain providers might implement a table on top of a binary tree, treating the table's halfway point as the top of the tree for performance reasons.</span></span> <span data-ttu-id="e1563-123">ツリーのバランスがとれていない場合、使用される中間点があります、表の途中で正確に。</span><span class="sxs-lookup"><span data-stu-id="e1563-123">If the tree is not balanced, then the halfway point used might not be exactly halfway through the table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e1563-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e1563-124">Notes to callers</span></span>

<span data-ttu-id="e1563-125">スクロール バーの実装にデータを提供する**SeekRowApprox**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e1563-125">Call **SeekRowApprox** to provide the data for a scroll bar implementation.</span></span> <span data-ttu-id="e1563-126">などの場合は、スクロール ボックス 2 と 3、スクロール バーを置くと、そのアクションをモデル**SeekRowApprox**を呼び出すと、 _ulNumerator_と_ulDenominator_を使用して同等の小数部から成る値を渡すことによって。</span><span class="sxs-lookup"><span data-stu-id="e1563-126">For example, if the user positions the scroll box 2/3 down the scroll bar, you can model that action by calling **SeekRowApprox** and passing in an equivalent fractional value using  _ulNumerator_ and  _ulDenominator_.</span></span> <span data-ttu-id="e1563-127">**SeekRowApprox**の検索では、テーブルの先頭からの絶対常にします。</span><span class="sxs-lookup"><span data-stu-id="e1563-127">The **SeekRowApprox** search is always absolute from the beginning of the table.</span></span> <span data-ttu-id="e1563-128">テーブルの末尾に移動するには、 _ulNumerator_と_ulDenominator_の値は同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1563-128">To move to the end of the table, the values in  _ulNumerator_ and  _ulDenominator_ must be the same.</span></span> 
  
<span data-ttu-id="e1563-129">適切な任意の数のスキームを使用します。</span><span class="sxs-lookup"><span data-stu-id="e1563-129">Use whatever number scheme is appropriate.</span></span> <span data-ttu-id="e1563-130">テーブルを中間の位置にシークに、1/2、10 月 20、または 50 または 100 を指定できます。</span><span class="sxs-lookup"><span data-stu-id="e1563-130">That is, to seek to a position halfway through the table, you can specify 1/2, 10/20, or 50/100.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1563-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1563-131">See also</span></span>



[<span data-ttu-id="e1563-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1563-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

