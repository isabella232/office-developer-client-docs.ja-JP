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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bbb79097d03a8ea09cb4aff374231ee780e15395
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412150"
---
# <a name="imapitableseekrowapprox"></a><span data-ttu-id="97b46-103">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="97b46-103">IMAPITable::SeekRowApprox</span></span>

  
  
<span data-ttu-id="97b46-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97b46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97b46-105">カーソルをテーブル内のおおよその小数位置に移動します。</span><span class="sxs-lookup"><span data-stu-id="97b46-105">Moves the cursor to an approximate fractional position in the table.</span></span> 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="97b46-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97b46-106">Parameters</span></span>

 <span data-ttu-id="97b46-107">_ulNumerator_</span><span class="sxs-lookup"><span data-stu-id="97b46-107">_ulNumerator_</span></span>
  
> <span data-ttu-id="97b46-108">[in]表の位置を表す分数の分子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="97b46-108">[in] Pointer to the numerator of the fraction representing the table position.</span></span> <span data-ttu-id="97b46-109">_ulNumerator パラメーターが 0_ の場合、分母の値に関係なく、カーソルはテーブルの先頭に配置されます。</span><span class="sxs-lookup"><span data-stu-id="97b46-109">If the  _ulNumerator_ parameter is zero, the cursor is positioned at the beginning of the table regardless of the denominator value.</span></span> <span data-ttu-id="97b46-110">_ulNumerator が_ _ulDenominator_ パラメーターと等しい場合、カーソルは最後のテーブル行の後に配置されます。</span><span class="sxs-lookup"><span data-stu-id="97b46-110">If  _ulNumerator_ is equal to the  _ulDenominator_ parameter, the cursor is positioned after the last table row.</span></span> 
    
 <span data-ttu-id="97b46-111">_ulDenominator_</span><span class="sxs-lookup"><span data-stu-id="97b46-111">_ulDenominator_</span></span>
  
> <span data-ttu-id="97b46-112">[in]表の位置を表す分数の分母へのポインター。</span><span class="sxs-lookup"><span data-stu-id="97b46-112">[in] Pointer to the denominator of the fraction representing the table position.</span></span> <span data-ttu-id="97b46-113">_ulDenominator パラメーター_ は 0 にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="97b46-113">The  _ulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="97b46-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="97b46-114">Return value</span></span>

<span data-ttu-id="97b46-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="97b46-115">S_OK</span></span> 
  
> <span data-ttu-id="97b46-116">シーク操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="97b46-116">The seek operation was successful.</span></span>
    
<span data-ttu-id="97b46-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="97b46-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="97b46-118">行シーク操作が開始されるのを防ぐ別の操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="97b46-118">Another operation is in progress that prevents the row seeking operation from starting.</span></span> <span data-ttu-id="97b46-119">進行中の操作の完了を許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97b46-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97b46-120">注釈</span><span class="sxs-lookup"><span data-stu-id="97b46-120">Remarks</span></span>

<span data-ttu-id="97b46-121">**IMAPITable::SeekRowApprox** メソッドの呼び出し後のテーブル内のカーソル位置は、ヒューリスティックに分数であり、正確ではない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="97b46-121">The cursor position in a table after a call to the **IMAPITable::SeekRowApprox** method is heuristically the fraction and might not be exact.</span></span> <span data-ttu-id="97b46-122">たとえば、特定のプロバイダーはバイナリ ツリーの上にテーブルを実装し、パフォーマンス上の理由からテーブルの中途半端な位置をツリーの上端として扱う場合があります。</span><span class="sxs-lookup"><span data-stu-id="97b46-122">For example, certain providers might implement a table on top of a binary tree, treating the table's halfway point as the top of the tree for performance reasons.</span></span> <span data-ttu-id="97b46-123">ツリーのバランスが取されていない場合、使用される中途半端なポイントがテーブルの正確な途中ではない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="97b46-123">If the tree is not balanced, then the halfway point used might not be exactly halfway through the table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="97b46-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="97b46-124">Notes to callers</span></span>

<span data-ttu-id="97b46-125">**SeekRowApprox を呼び** 出して、スクロール バーの実装のデータを提供します。</span><span class="sxs-lookup"><span data-stu-id="97b46-125">Call **SeekRowApprox** to provide the data for a scroll bar implementation.</span></span> <span data-ttu-id="97b46-126">たとえば、スクロール ボックスをスクロール バーの 2/3 下に配置する場合は **、SeekRowApprox** を呼び出し  _、ulNumerator_ と  _ulDenominator_ を使用して同等の小数部の値を渡すことによって、そのアクションをモデル化できます。</span><span class="sxs-lookup"><span data-stu-id="97b46-126">For example, if the user positions the scroll box 2/3 down the scroll bar, you can model that action by calling **SeekRowApprox** and passing in an equivalent fractional value using  _ulNumerator_ and  _ulDenominator_.</span></span> <span data-ttu-id="97b46-127">**SeekRowApprox 検索** は、常にテーブルの先頭から絶対値です。</span><span class="sxs-lookup"><span data-stu-id="97b46-127">The **SeekRowApprox** search is always absolute from the beginning of the table.</span></span> <span data-ttu-id="97b46-128">表の末尾に移動するには  _、ulNumerator_ と  _ulDenominator_ の値が同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="97b46-128">To move to the end of the table, the values in  _ulNumerator_ and  _ulDenominator_ must be the same.</span></span> 
  
<span data-ttu-id="97b46-129">適切な番号スキームを使用します。</span><span class="sxs-lookup"><span data-stu-id="97b46-129">Use whatever number scheme is appropriate.</span></span> <span data-ttu-id="97b46-130">つまり、テーブルの途中の位置をシークするには、1/2、10/20、または 50/100 を指定できます。</span><span class="sxs-lookup"><span data-stu-id="97b46-130">That is, to seek to a position halfway through the table, you can specify 1/2, 10/20, or 50/100.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97b46-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="97b46-131">See also</span></span>



[<span data-ttu-id="97b46-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="97b46-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

