---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2e44d824bbb5cc96c51d7ca91eb639001bc52a71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415664"
---
# <a name="imapitablequeryposition"></a><span data-ttu-id="966d8-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="966d8-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="966d8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="966d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="966d8-105">小数部の値に基づいて、カーソルの現在のテーブル行の位置を取得します。</span><span class="sxs-lookup"><span data-stu-id="966d8-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="966d8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="966d8-106">Parameters</span></span>

 <span data-ttu-id="966d8-107">_lpulRow_</span><span class="sxs-lookup"><span data-stu-id="966d8-107">_lpulRow_</span></span>
  
> <span data-ttu-id="966d8-108">[out]現在の行の番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="966d8-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="966d8-109">行番号は 0 から始ります。テーブルの最初の行は 0 です。</span><span class="sxs-lookup"><span data-stu-id="966d8-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="966d8-110">_lpulNumerator_</span><span class="sxs-lookup"><span data-stu-id="966d8-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="966d8-111">[out]表の位置を識別する分数の分子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="966d8-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="966d8-112">_lpulDenominator_</span><span class="sxs-lookup"><span data-stu-id="966d8-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="966d8-113">[out]テーブル位置を識別する分数の分母へのポインター。</span><span class="sxs-lookup"><span data-stu-id="966d8-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="966d8-114">_lpulDenominator パラメーター_ は 0 にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="966d8-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="966d8-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="966d8-115">Return value</span></span>

<span data-ttu-id="966d8-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="966d8-116">S_OK</span></span> 
  
> <span data-ttu-id="966d8-117">メソッドは  _、lpulRow_  _、lpulNumerator、および_  _lpulDenominator で有効な値を返しました_。</span><span class="sxs-lookup"><span data-stu-id="966d8-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="966d8-118">注釈</span><span class="sxs-lookup"><span data-stu-id="966d8-118">Remarks</span></span>

<span data-ttu-id="966d8-119">**IMAPITable::QueryPosition** メソッドは、現在の行の位置を決定し、現在の行の番号と、テーブルの末尾への相対位置を示す小数部の値の両方を返します。</span><span class="sxs-lookup"><span data-stu-id="966d8-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="966d8-120">MAPI は、現在の行を読み取る次の行として定義します。</span><span class="sxs-lookup"><span data-stu-id="966d8-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="966d8-121">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="966d8-121">Notes to implementers</span></span>

<span data-ttu-id="966d8-122">_lpulDenominator_ パラメーターのテーブル内の行の正確な数を返す必要があります。近似値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="966d8-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="966d8-123">現在の行を特定できない場合は  _、lpulRow_ の値0xFFFFFFFF返します。</span><span class="sxs-lookup"><span data-stu-id="966d8-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="966d8-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="966d8-124">Notes to callers</span></span>

<span data-ttu-id="966d8-125">QueryPosition を **使用すると** 、スクロール バーにスクロール ボックスを配置できます。</span><span class="sxs-lookup"><span data-stu-id="966d8-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="966d8-126">たとえば、100 行を含むテーブルで **、QueryPosition** が _lpulNumerator_ パラメーターで 75、lpulDenominator パラメーターで 100、lpulRow パラメーターに75 の値を返す場合、スクロール バーを横切る方向のスクロール ボックス 3/4 を配置できます。</span><span class="sxs-lookup"><span data-stu-id="966d8-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="966d8-127">_lpulDenominator_ の値がテーブル内の行数に依存しない。</span><span class="sxs-lookup"><span data-stu-id="966d8-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="966d8-128">**QueryPosition** では、カーソルが配置されている正確な行を常に特定できません。</span><span class="sxs-lookup"><span data-stu-id="966d8-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="966d8-129">QueryPosition の呼 **び出** しには、特に大きな分類テーブルに対して大量のメモリが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="966d8-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="966d8-130">_lpulRow パラメーターが_ 現在の行に設定されている **0xFFFFFFFF、QueryPosition** で現在の行を決定するために必要なメモリが多すぎます。</span><span class="sxs-lookup"><span data-stu-id="966d8-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="966d8-131">[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)メソッドを呼び出して _、lpulNumerator_ パラメーターと _lpulDenominator_ パラメーターで識別される行にテーブルを配置します。</span><span class="sxs-lookup"><span data-stu-id="966d8-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="966d8-132">ただし、メモリが要因ではない場合 **、SeekRowApprox** が現在の位置と同じ行 **QueryPosition** として確立されるとは限らない。</span><span class="sxs-lookup"><span data-stu-id="966d8-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="966d8-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="966d8-133">See also</span></span>



[<span data-ttu-id="966d8-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="966d8-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="966d8-135">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="966d8-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

