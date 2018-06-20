---
title: IMAPIProgressGetMax
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bbd52116a108be12df7697f45df41b03adeba68e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800633"
---
# <a name="imapiprogressgetmax"></a><span data-ttu-id="0f4ea-103">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="0f4ea-103">IMAPIProgress::GetMax</span></span>

  
  
<span data-ttu-id="0f4ea-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f4ea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f4ea-105">情報を表示する進行中の操作では、アイテムの最大数を返します。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-105">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a><span data-ttu-id="0f4ea-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0f4ea-106">Parameters</span></span>

 <span data-ttu-id="0f4ea-107">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="0f4ea-107">_lpulMax_</span></span>
  
> <span data-ttu-id="0f4ea-108">[out]操作内のアイテムの最大数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-108">[out] A pointer to the maximum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0f4ea-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0f4ea-109">Return value</span></span>

<span data-ttu-id="0f4ea-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f4ea-110">S_OK</span></span> 
  
> <span data-ttu-id="0f4ea-111">操作内のアイテムの最大数を取得するとします。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-111">The maximum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f4ea-112">備考</span><span class="sxs-lookup"><span data-stu-id="0f4ea-112">Remarks</span></span>

<span data-ttu-id="0f4ea-113">最大値は、数値形式での操作の終了を表します。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-113">The maximum value represents the end of the operation in numeric form.</span></span> <span data-ttu-id="0f4ea-114">値は、全体の進行状況表示の範囲を表すために使用、グローバルな最大値またはローカル値になっているため、画面の一部のみを表すために使用できます。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="0f4ea-115">フラグの設定の値は、実行中のオブジェクトは、ローカルまたはグローバルに最大の価値を理解しているかどうかに影響します。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-115">The value of the flag setting affects whether the progress object understands the maximum value to be local or global.</span></span> <span data-ttu-id="0f4ea-116">MAPI_TOP_LEVEL フラグを設定すると最大値はグローバルと見なされ、処理全体の進行状況を計算するために使用します。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-116">When the MAPI_TOP_LEVEL flag is set, the maximum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="0f4ea-117">MAPI_TOP_LEVEL が設定されていないと最大値と見なされる、ローカル プロバイダーを使用して、内部的に低レベルのサブオブジェクトの進行状況を表示します。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-117">When MAPI_TOP_LEVEL is not set, the maximum value is considered to be local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="0f4ea-118">進行中のオブジェクトは、 **GetMax**の呼び出しを使用して、プロバイダーに戻す場合にのみローカル最大値を保存します。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-118">Progress objects save the local maximum value only to return it to a provider through a **GetMax** call.</span></span> 
  
<span data-ttu-id="0f4ea-119">方法の詳細については、実行中のオブジェクトへの呼び出しを行う場合は、[進行状況のインジケーターの表示](how-to-display-a-progress-indicator.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-119">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0f4ea-120">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="0f4ea-120">Notes to implementers</span></span>

<span data-ttu-id="0f4ea-121">1000 の最大値を初期化します。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-121">Initialize the maximum value to 1000.</span></span> <span data-ttu-id="0f4ea-122">サービス プロバイダーは、 [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)メソッドを呼び出すことによって、この値をリセットできます。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-122">Service providers can reset this value by calling the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> <span data-ttu-id="0f4ea-123">**GetMax**およびその他の[IMAPIProgress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、[進行状況のインジケーターを実装する](implementing-a-progress-indicator.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-123">For more information about how to implement **GetMax** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0f4ea-124">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="0f4ea-124">MFCMAPI reference</span></span>

<span data-ttu-id="0f4ea-125">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="0f4ea-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0f4ea-126">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="0f4ea-126">**File**</span></span>|<span data-ttu-id="0f4ea-127">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="0f4ea-127">**Function**</span></span>|<span data-ttu-id="0f4ea-128">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="0f4ea-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0f4ea-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="0f4ea-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="0f4ea-130">CMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="0f4ea-130">CMAPIProgress::GetMax</span></span>  <br/> |<span data-ttu-id="0f4ea-131">MFCMAPI では、 **IMAPIProgress::GetMax**メソッドを使用して、実行中のオブジェクトの最大値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-131">MFCMAPI uses the **IMAPIProgress::GetMax** method to get the maximum value for the progress object.</span></span> <span data-ttu-id="0f4ea-132">**IMAPIProgress::SetLimits**メソッドでの制限が既に設定されていない限り、1000 を返します。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-132">Returns 1000 unless limits have previously been set with the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0f4ea-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f4ea-133">See also</span></span>



[<span data-ttu-id="0f4ea-134">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="0f4ea-134">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="0f4ea-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="0f4ea-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="0f4ea-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="0f4ea-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="0f4ea-137">IMAPIProgress: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0f4ea-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


<span data-ttu-id="0f4ea-138">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="0f4ea-138">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="0f4ea-139">進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="0f4ea-140">進行状況のインジケーターを実装します。</span><span class="sxs-lookup"><span data-stu-id="0f4ea-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

