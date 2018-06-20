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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c3c66b9e54f0776a8afd6b4638d36dec3393dda8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800841"
---
# <a name="imapitablequeryposition"></a><span data-ttu-id="bbe57-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="bbe57-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="bbe57-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bbe57-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bbe57-105">小数部の値に基づいて、カーソルの現在のテーブルの行位置を取得します。</span><span class="sxs-lookup"><span data-stu-id="bbe57-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="bbe57-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="bbe57-106">Parameters</span></span>

 <span data-ttu-id="bbe57-107">_lpulRow_</span><span class="sxs-lookup"><span data-stu-id="bbe57-107">_lpulRow_</span></span>
  
> <span data-ttu-id="bbe57-108">[out]現在の行の行番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bbe57-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="bbe57-109">行番号は 0 から始まります。テーブルの最初の行は 0 です。</span><span class="sxs-lookup"><span data-stu-id="bbe57-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="bbe57-110">_lpulNumerator_</span><span class="sxs-lookup"><span data-stu-id="bbe57-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="bbe57-111">[out]テーブルの位置を識別する分数の分子の部分へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bbe57-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="bbe57-112">_lpulDenominator_</span><span class="sxs-lookup"><span data-stu-id="bbe57-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="bbe57-113">[out]テーブルの位置を識別する分数の分母となるへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bbe57-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="bbe57-114">_LpulDenominator_パラメーターは、ゼロにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="bbe57-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bbe57-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="bbe57-115">Return value</span></span>

<span data-ttu-id="bbe57-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="bbe57-116">S_OK</span></span> 
  
> <span data-ttu-id="bbe57-117">メソッドでは、 _lpulRow_、 _lpulNumerator_、 _lpulDenominator_で有効な値が返されます。</span><span class="sxs-lookup"><span data-stu-id="bbe57-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bbe57-118">備考</span><span class="sxs-lookup"><span data-stu-id="bbe57-118">Remarks</span></span>

<span data-ttu-id="bbe57-119">**IMAPITable::QueryPosition**メソッドは、現在の行位置を指定し、現在の行とテーブルの末尾には、相対的な位置を示す小数部の値の番号の両方を返します。</span><span class="sxs-lookup"><span data-stu-id="bbe57-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="bbe57-120">MAPI は、読み取られる次の行として、現在の行を定義します。</span><span class="sxs-lookup"><span data-stu-id="bbe57-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bbe57-121">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="bbe57-121">Notes to implementers</span></span>

<span data-ttu-id="bbe57-122">_LpulDenominator_パラメーターのテーブルの行の正確な数を取得する必要はありません。概算値となります。</span><span class="sxs-lookup"><span data-stu-id="bbe57-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="bbe57-123">、現在の行を特定できない場合は、 _lpulRow_に 0 xffffffff の値を返します。</span><span class="sxs-lookup"><span data-stu-id="bbe57-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="bbe57-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="bbe57-124">Notes to callers</span></span>

<span data-ttu-id="bbe57-125">**QueryPosition**を使用すると、スクロール バーのスクロール ボックスを配置します。</span><span class="sxs-lookup"><span data-stu-id="bbe57-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="bbe57-126">100 行を含むテーブルでの**QueryPosition**は、 _lpulDenominator_パラメーターに 100、75、 _lpulRow_パラメーターで、 _lpulNumerator_パラメーターで 75 の値を返す場合は、スクロール ボックス 3/4 を配置することスクロール バーの間での方法です。</span><span class="sxs-lookup"><span data-stu-id="bbe57-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="bbe57-127">テーブル内の行の数をされている_lpulDenominator_の値に依存しません。</span><span class="sxs-lookup"><span data-stu-id="bbe57-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="bbe57-128">**QueryPosition**は、正確な行にカーソルが配置されていることを常に識別できません。</span><span class="sxs-lookup"><span data-stu-id="bbe57-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="bbe57-129">**QueryPosition**への呼び出しには、大量メモリ、特に大規模な分類されたテーブルにはが含まれます。</span><span class="sxs-lookup"><span data-stu-id="bbe57-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="bbe57-130">_LpulRow_パラメーターは、0 xffffffff に設定されている場合、大量のメモリは**QueryPosition**を現在の行を特定するために必要でした。</span><span class="sxs-lookup"><span data-stu-id="bbe57-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="bbe57-131">_LpulNumerator_および_lpulDenominator_パラメーターで指定された行にテーブルを配置する[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bbe57-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="bbe57-132">ただし、常にされないように**QueryPosition**がメモリが倍にしていない場合、同じ行を現在の位置として確立するために**SeekRowApprox** 。</span><span class="sxs-lookup"><span data-stu-id="bbe57-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bbe57-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="bbe57-133">See also</span></span>



[<span data-ttu-id="bbe57-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="bbe57-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="bbe57-135">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bbe57-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

