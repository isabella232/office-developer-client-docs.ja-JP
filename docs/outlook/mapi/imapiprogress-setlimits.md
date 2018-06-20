---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 14abfaadcdb1710a7cb8275c8f82d502aea8300e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800641"
---
# <a name="imapiprogresssetlimits"></a><span data-ttu-id="20a90-103">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="20a90-103">IMAPIProgress::SetLimits</span></span>

  
  
<span data-ttu-id="20a90-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20a90-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20a90-105">操作、および操作の進行状況の情報を計算する方法を制御するフラグでは、アイテム数の上限と下限の制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="20a90-105">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="20a90-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="20a90-106">Parameters</span></span>

 <span data-ttu-id="20a90-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="20a90-107">_lpulMin_</span></span>
  
> <span data-ttu-id="20a90-108">[in]操作内の項目の最小値を含む変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="20a90-108">[in] A pointer to a variable that contains the lower limit of items in the operation.</span></span>
    
 <span data-ttu-id="20a90-109">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="20a90-109">_lpulMax_</span></span>
  
> <span data-ttu-id="20a90-110">[in]操作内の項目の最大値を含む変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="20a90-110">[in] A pointer to a variable that contains the upper limit of items in the operation.</span></span>
    
 <span data-ttu-id="20a90-111">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="20a90-111">_lpulFlags_</span></span>
  
> <span data-ttu-id="20a90-112">[in]進捗状況の情報を計算する操作のレベルを制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="20a90-112">[in] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="20a90-113">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="20a90-113">The following flag can be set:</span></span>
    
<span data-ttu-id="20a90-114">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="20a90-114">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="20a90-115">[IMAPIProgress::Progress](imapiprogress-progress.md)メソッドの_ulCount_および_ulTotal_パラメーターで、操作の進行状況をインクリメント、それぞれ、現在処理済みのアイテムとアイテムの合計を示す値を使用します。</span><span class="sxs-lookup"><span data-stu-id="20a90-115">Uses the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters, which indicate the currently processed item and the total items, respectively, to increment progress on the operation.</span></span> <span data-ttu-id="20a90-116">このフラグを設定すると、グローバルの上限と下限の制限の値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20a90-116">When this flag is set, the values of the global lower and upper limits have to be set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="20a90-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="20a90-117">Return value</span></span>

<span data-ttu-id="20a90-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="20a90-118">S_OK</span></span> 
  
> <span data-ttu-id="20a90-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="20a90-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20a90-120">����</span><span class="sxs-lookup"><span data-stu-id="20a90-120">Remarks</span></span>

<span data-ttu-id="20a90-121">サービス プロバイダーは、ローカルおよびグローバルの最小値と最大値を設定して、MAPI_TOP_LEVEL フラグを設定または**IMAPIProgress::SetLimits**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="20a90-121">Service providers call the **IMAPIProgress::SetLimits** method to set or clear the MAPI_TOP_LEVEL flag and to set local and global minimum and maximum values.</span></span> <span data-ttu-id="20a90-122">フラグの設定の値は、実行中のオブジェクトは、最小値と最大値は、ローカルまたはグローバルを理解しているかどうかに影響します。</span><span class="sxs-lookup"><span data-stu-id="20a90-122">The value of the flag setting affects whether the progress object understands the minimum and maximum values to be local or global.</span></span> <span data-ttu-id="20a90-123">MAPI_TOP_LEVEL フラグを設定すると、これらの値はグローバルと見なされ、全体の操作の進行状況を計算するために使用します。</span><span class="sxs-lookup"><span data-stu-id="20a90-123">When the MAPI_TOP_LEVEL flag is set, these values are considered global and are used to calculate progress for the entire operation.</span></span> <span data-ttu-id="20a90-124">進行中のオブジェクトでは、グローバルの最小値を 1 と 1000 のグローバル最大値を初期化します。</span><span class="sxs-lookup"><span data-stu-id="20a90-124">Progress objects initialize the global minimum value to 1 and the global maximum value to 1000.</span></span> 
  
<span data-ttu-id="20a90-125">MAPI_TOP_LEVEL が設定されていない場合、最小値と最大値は、ローカルと見なされます、プロバイダーに内部的に使用して低レベルのサブオブジェクトの進行状況を表示します。</span><span class="sxs-lookup"><span data-stu-id="20a90-125">When MAPI_TOP_LEVEL is not set, the minimum and maximum values are considered local, and providers use them internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="20a90-126">進行中のオブジェクトは、 [IMAPIProgress::GetMin](imapiprogress-getmin.md)メソッドと[IMAPIProgress::GetMax](imapiprogress-getmax.md)メソッドが呼び出されたときにプロバイダーに返すことができますようにするためだけにローカルの最小値と最大値を保存します。</span><span class="sxs-lookup"><span data-stu-id="20a90-126">Progress objects save the local minimum and maximum values only so that they can be returned to providers when the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods are called.</span></span> 
  
<span data-ttu-id="20a90-127">**SetLimits**およびその他の[IMAPIProgress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、[進行状況のインジケーターを実装する](implementing-a-progress-indicator.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20a90-127">For more information about how to implement **SetLimits** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="20a90-128">方法の詳細については、実行中のオブジェクトへの呼び出しを行う場合は、[進行状況のインジケーターの表示](how-to-display-a-progress-indicator.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20a90-128">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="20a90-129">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="20a90-129">MFCMAPI reference</span></span>

<span data-ttu-id="20a90-130">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="20a90-130">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="20a90-131">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="20a90-131">**File**</span></span>|<span data-ttu-id="20a90-132">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="20a90-132">**Function**</span></span>|<span data-ttu-id="20a90-133">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="20a90-133">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="20a90-134">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="20a90-134">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="20a90-135">CMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="20a90-135">CMAPIProgress::SetLimits</span></span>  <br/> |<span data-ttu-id="20a90-136">MFCMAPI では、 **IMAPIProgress::SetLimits**メソッドを使用して、上限と下限と進行中のオブジェクトのフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="20a90-136">MFCMAPI uses the **IMAPIProgress::SetLimits** method to set the maximum and minimum limits and flags for the progress object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20a90-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="20a90-137">See also</span></span>



[<span data-ttu-id="20a90-138">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="20a90-138">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="20a90-139">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="20a90-139">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="20a90-140">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="20a90-140">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="20a90-141">IMAPIProgress: IUnknown</span><span class="sxs-lookup"><span data-stu-id="20a90-141">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


<span data-ttu-id="20a90-142">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="20a90-142">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="20a90-143">進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="20a90-143">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="20a90-144">進行状況のインジケーターを実装します。</span><span class="sxs-lookup"><span data-stu-id="20a90-144">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

