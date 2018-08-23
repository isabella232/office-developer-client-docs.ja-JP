---
title: IMAPIProgressGetMin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMin
api_type:
- COM
ms.assetid: caceddf1-0f7c-47b5-97bf-17ffe3440a6c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ab92aee6a8254a16c48352e371b711932bbe7427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800636"
---
# <a name="imapiprogressgetmin"></a><span data-ttu-id="02f98-103">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="02f98-103">IMAPIProgress::GetMin</span></span>

  
  
<span data-ttu-id="02f98-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="02f98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="02f98-105">進捗状況の情報が表示されます、 [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)メソッドでは、最小値を返します。</span><span class="sxs-lookup"><span data-stu-id="02f98-105">Returns the minimum value in the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span> 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a><span data-ttu-id="02f98-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="02f98-106">Parameters</span></span>

 <span data-ttu-id="02f98-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="02f98-107">_lpulMin_</span></span>
  
> <span data-ttu-id="02f98-108">[out]操作内のアイテムの最小数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="02f98-108">[out] A pointer to the minimum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="02f98-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="02f98-109">Return value</span></span>

<span data-ttu-id="02f98-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="02f98-110">S_OK</span></span> 
  
> <span data-ttu-id="02f98-111">操作内のアイテムの最小数を取得するとします。</span><span class="sxs-lookup"><span data-stu-id="02f98-111">The minimum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="02f98-112">注釈</span><span class="sxs-lookup"><span data-stu-id="02f98-112">Remarks</span></span>

<span data-ttu-id="02f98-113">最小値は、数値形式での操作の開始を表します。</span><span class="sxs-lookup"><span data-stu-id="02f98-113">The minimum value represents the start of the operation in numeric form.</span></span> <span data-ttu-id="02f98-114">値は、全体の進行状況表示の範囲を表すために使用、グローバルな最大値またはローカル値になっているため、画面の一部のみを表すために使用できます。</span><span class="sxs-lookup"><span data-stu-id="02f98-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="02f98-115">フラグの設定の値は、実行中のオブジェクトは、ローカルまたはグローバルに最小値を理解しているかどうかに影響します。</span><span class="sxs-lookup"><span data-stu-id="02f98-115">The value of the flag setting affects whether the progress object understands the minimum value to be local or global.</span></span> <span data-ttu-id="02f98-116">MAPI_TOP_LEVEL フラグを設定すると、最小値はグローバルと見なされ、処理全体の進行状況を計算するために使用します。</span><span class="sxs-lookup"><span data-stu-id="02f98-116">When the MAPI_TOP_LEVEL flag is set, the minimum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="02f98-117">MAPI_TOP_LEVEL が設定されていないと最小値は、ローカルと見なされるプロバイダーを使用して、内部的に低レベルのサブオブジェクトの進行状況を表示します。</span><span class="sxs-lookup"><span data-stu-id="02f98-117">When MAPI_TOP_LEVEL is not set, the minimum value is considered local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="02f98-118">進行中のオブジェクトは、 **GetMin**の呼び出しを使用して、プロバイダーに戻す場合にのみローカルの最小値を保存します。</span><span class="sxs-lookup"><span data-stu-id="02f98-118">Progress objects save the local minimum value only to return it to a provider through a **GetMin** call.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="02f98-119">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="02f98-119">Notes to implementers</span></span>

<span data-ttu-id="02f98-120">1 に最小値を初期化します。</span><span class="sxs-lookup"><span data-stu-id="02f98-120">Initialize the minimum value to 1.</span></span> <span data-ttu-id="02f98-121">サービス プロバイダーは、 **IMAPIProgress::SetLimits**メソッドを呼び出すことによって、この値をリセットできます。</span><span class="sxs-lookup"><span data-stu-id="02f98-121">Service providers can reset this value by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="02f98-122">**GetMin**およびその他の[IMAPIProgress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、[進行状況のインジケーターを実装する](implementing-a-progress-indicator.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02f98-122">For more information about how to implement **GetMin** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="02f98-123">方法の詳細については、実行中のオブジェクトへの呼び出しを行う場合は、[進行状況のインジケーターの表示](how-to-display-a-progress-indicator.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02f98-123">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="02f98-124">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="02f98-124">MFCMAPI reference</span></span>

<span data-ttu-id="02f98-125">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="02f98-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="02f98-126">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="02f98-126">**File**</span></span>|<span data-ttu-id="02f98-127">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="02f98-127">**Function**</span></span>|<span data-ttu-id="02f98-128">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="02f98-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="02f98-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="02f98-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="02f98-130">CMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="02f98-130">CMAPIProgress::GetMin</span></span>  <br/> |<span data-ttu-id="02f98-131">MFCMAPI では、 **IMAPIProgress::GetMin**メソッドを使用して、進行状況インジケーターの最小値を取得します。</span><span class="sxs-lookup"><span data-stu-id="02f98-131">MFCMAPI uses the **IMAPIProgress::GetMin** method to get the minimum value for the progress indicator.</span></span> <span data-ttu-id="02f98-132">制限は、 **IMAPIProgress::SetLimits**メソッドを呼び出すことですでに設定されている場合を除き、1 を返します。</span><span class="sxs-lookup"><span data-stu-id="02f98-132">Returns 1 unless limits have been previously set by calling the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02f98-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="02f98-133">See also</span></span>



[<span data-ttu-id="02f98-134">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="02f98-134">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="02f98-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="02f98-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="02f98-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="02f98-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="02f98-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="02f98-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


<span data-ttu-id="02f98-138">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="02f98-138">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="02f98-139">進行状況インジケーターを表示する</span><span class="sxs-lookup"><span data-stu-id="02f98-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="02f98-140">進行状況インジケーターの実装</span><span class="sxs-lookup"><span data-stu-id="02f98-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

