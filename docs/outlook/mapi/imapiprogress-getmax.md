---
title: imapi進捗 getmax
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMax
api_type:
- COM
ms.assetid: 88a910ed-b55a-4e5b-a43d-eb3ea795a70e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 64b6235151c7700a24992bc1d4394553a53c0464
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270204"
---
# <a name="imapiprogressgetmax"></a><span data-ttu-id="7c31e-103">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="7c31e-103">IMAPIProgress::GetMax</span></span>

  
  
<span data-ttu-id="7c31e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c31e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c31e-105">進行状況の情報が表示される操作内のアイテムの最大数を返します。</span><span class="sxs-lookup"><span data-stu-id="7c31e-105">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a><span data-ttu-id="7c31e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7c31e-106">Parameters</span></span>

 <span data-ttu-id="7c31e-107">_lプル最大_</span><span class="sxs-lookup"><span data-stu-id="7c31e-107">_lpulMax_</span></span>
  
> <span data-ttu-id="7c31e-108">読み上げ操作内のアイテムの最大数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7c31e-108">[out] A pointer to the maximum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c31e-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="7c31e-109">Return value</span></span>

<span data-ttu-id="7c31e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c31e-110">S_OK</span></span> 
  
> <span data-ttu-id="7c31e-111">操作内のアイテムの最大数が取得されました。</span><span class="sxs-lookup"><span data-stu-id="7c31e-111">The maximum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c31e-112">解説</span><span class="sxs-lookup"><span data-stu-id="7c31e-112">Remarks</span></span>

<span data-ttu-id="7c31e-113">最大値は、操作の終了を数値形式で表します。</span><span class="sxs-lookup"><span data-stu-id="7c31e-113">The maximum value represents the end of the operation in numeric form.</span></span> <span data-ttu-id="7c31e-114">値は、進行状況の表示全体の範囲を示すために使用されるグローバルな最大値、あるいは表示の一部のみを示すのに使用されるローカル値になります。</span><span class="sxs-lookup"><span data-stu-id="7c31e-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="7c31e-115">flag 設定の値は、progress オブジェクトがローカルまたはグローバルに最大値を認識しているかどうかに影響します。</span><span class="sxs-lookup"><span data-stu-id="7c31e-115">The value of the flag setting affects whether the progress object understands the maximum value to be local or global.</span></span> <span data-ttu-id="7c31e-116">MAPI_TOP_LEVEL フラグが設定されている場合、最大値はグローバルと見なされ、操作全体の進行状況を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7c31e-116">When the MAPI_TOP_LEVEL flag is set, the maximum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="7c31e-117">MAPI_TOP_LEVEL が設定されていない場合、最大値はローカルと見なされ、プロバイダーはそれを内部的に使用して、下位レベルのサブオブジェクトの進行状況を表示します。</span><span class="sxs-lookup"><span data-stu-id="7c31e-117">When MAPI_TOP_LEVEL is not set, the maximum value is considered to be local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="7c31e-118">Progress オブジェクトは、 **getmax**呼び出しを通じてプロバイダーに返すためだけにローカル最大値を保存します。</span><span class="sxs-lookup"><span data-stu-id="7c31e-118">Progress objects save the local maximum value only to return it to a provider through a **GetMax** call.</span></span> 
  
<span data-ttu-id="7c31e-119">進行状況オブジェクトを呼び出す方法とタイミングの詳細については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c31e-119">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7c31e-120">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="7c31e-120">Notes to implementers</span></span>

<span data-ttu-id="7c31e-121">最大値を1000に初期化します。</span><span class="sxs-lookup"><span data-stu-id="7c31e-121">Initialize the maximum value to 1000.</span></span> <span data-ttu-id="7c31e-122">サービス プロバイダーは、[IMAPIProgress::SetLimits](imapiprogress-setlimits.md) メソッドを呼び出してこの値をリセットできます。</span><span class="sxs-lookup"><span data-stu-id="7c31e-122">Service providers can reset this value by calling the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> <span data-ttu-id="7c31e-123">**getmax**およびその他の[imapiprogress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、「[進行状況インジケーターの実装](implementing-a-progress-indicator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c31e-123">For more information about how to implement **GetMax** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7c31e-124">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="7c31e-124">MFCMAPI reference</span></span>

<span data-ttu-id="7c31e-125">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c31e-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7c31e-126">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="7c31e-126">**File**</span></span>|<span data-ttu-id="7c31e-127">**関数**</span><span class="sxs-lookup"><span data-stu-id="7c31e-127">**Function**</span></span>|<span data-ttu-id="7c31e-128">**コメント**</span><span class="sxs-lookup"><span data-stu-id="7c31e-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7c31e-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="7c31e-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="7c31e-130">cmapiprogress 進行状況:: getmax</span><span class="sxs-lookup"><span data-stu-id="7c31e-130">CMAPIProgress::GetMax</span></span>  <br/> |<span data-ttu-id="7c31e-131">mfcmapi は、 **imapiprogress:: getmax**メソッドを使用して、progress オブジェクトの最大値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7c31e-131">MFCMAPI uses the **IMAPIProgress::GetMax** method to get the maximum value for the progress object.</span></span> <span data-ttu-id="7c31e-132">以前に**imapiprogress:: setlimits**メソッドを使用して制限が設定されていない場合は、1000を返します。</span><span class="sxs-lookup"><span data-stu-id="7c31e-132">Returns 1000 unless limits have previously been set with the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c31e-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c31e-133">See also</span></span>



[<span data-ttu-id="7c31e-134">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="7c31e-134">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="7c31e-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="7c31e-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="7c31e-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="7c31e-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="7c31e-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7c31e-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="7c31e-138">コード サンプルとしての MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7c31e-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="7c31e-139">進行状況インジケーターを表示する</span><span class="sxs-lookup"><span data-stu-id="7c31e-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="7c31e-140">進行状況インジケーターの実装</span><span class="sxs-lookup"><span data-stu-id="7c31e-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

