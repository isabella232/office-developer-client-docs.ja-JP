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
# <a name="imapitablequeryposition"></a><span data-ttu-id="b274f-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="b274f-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="b274f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b274f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b274f-105">小数値に基づいて、カーソルの現在のテーブル行の位置を取得します。</span><span class="sxs-lookup"><span data-stu-id="b274f-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="b274f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b274f-106">Parameters</span></span>

 <span data-ttu-id="b274f-107">_lの行_</span><span class="sxs-lookup"><span data-stu-id="b274f-107">_lpulRow_</span></span>
  
> <span data-ttu-id="b274f-108">読み上げ現在の行の番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b274f-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="b274f-109">行番号は0から始まります。表の最初の行は0になります。</span><span class="sxs-lookup"><span data-stu-id="b274f-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="b274f-110">_lアウト分子_</span><span class="sxs-lookup"><span data-stu-id="b274f-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="b274f-111">読み上げテーブルの位置を識別する分数の分子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b274f-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="b274f-112">_lアウト分母_</span><span class="sxs-lookup"><span data-stu-id="b274f-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="b274f-113">読み上げテーブルの位置を識別する分数の分母へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b274f-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="b274f-114">_lアウト分母_パラメーターを0にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b274f-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b274f-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="b274f-115">Return value</span></span>

<span data-ttu-id="b274f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b274f-116">S_OK</span></span> 
  
> <span data-ttu-id="b274f-117">メソッドは、 _lな行_の有効な値、l出た_分子_、および_lアウト分母_を返しました。</span><span class="sxs-lookup"><span data-stu-id="b274f-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b274f-118">注釈</span><span class="sxs-lookup"><span data-stu-id="b274f-118">Remarks</span></span>

<span data-ttu-id="b274f-119">**IMAPITable:: queryposition**メソッドは、現在の行の位置を決定し、現在の行の数と、テーブルの最後までの相対位置を示す小数値を返します。</span><span class="sxs-lookup"><span data-stu-id="b274f-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="b274f-120">MAPI は、現在の行を読み取る次の行として定義します。</span><span class="sxs-lookup"><span data-stu-id="b274f-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b274f-121">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="b274f-121">Notes to implementers</span></span>

<span data-ttu-id="b274f-122">_lアウト分母_パラメーターのテーブル内の行の正確な数を返す必要はありません。近似値になることがあります。</span><span class="sxs-lookup"><span data-stu-id="b274f-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="b274f-123">現在の行を特定できない場合は、 _lアウト row_で値0xffffffff を返します。</span><span class="sxs-lookup"><span data-stu-id="b274f-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b274f-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b274f-124">Notes to callers</span></span>

<span data-ttu-id="b274f-125">**queryposition**を使用して、スクロールバーのスクロールボックスを配置できます。</span><span class="sxs-lookup"><span data-stu-id="b274f-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="b274f-126">たとえば、100行を含むテーブルで、 **queryposition**が l出_分子_パラメーターで75の値を返し、l出_分母_パラメーターで100を返した場合は、スクロールボックス__ を次のように配置できます。をスクロールバーの上方向に移動します。</span><span class="sxs-lookup"><span data-stu-id="b274f-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="b274f-127">テーブル内の行の数として、 _lアウト分母_の値に依存しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="b274f-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="b274f-128">**queryposition**は、カーソルが置かれている正確な行を常に識別することはできません。</span><span class="sxs-lookup"><span data-stu-id="b274f-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="b274f-129">**queryposition**の呼び出しでは、特に、大きな分類されたテーブルの場合は、大量のメモリが関係することがあります。</span><span class="sxs-lookup"><span data-stu-id="b274f-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="b274f-130">lの_行_パラメーターが0xffffffff に設定されている場合、 **queryposition**が現在の行を特定するために必要なメモリの量が多すぎます。</span><span class="sxs-lookup"><span data-stu-id="b274f-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="b274f-131">[IMAPITable:: seekrowapprox](imapitable-seekrowapprox.md)メソッドを呼び出して、 _lpulnumerator_パラメーターと_lアウト分母_パラメーターで識別される行にテーブルを配置します。</span><span class="sxs-lookup"><span data-stu-id="b274f-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="b274f-132">ただし、メモリが係数で\*\*\*\* ない場合は、同じ行**queryposition**が現在の位置として設定されていると常に期待してはいけません。</span><span class="sxs-lookup"><span data-stu-id="b274f-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b274f-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="b274f-133">See also</span></span>



[<span data-ttu-id="b274f-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="b274f-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="b274f-135">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b274f-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

