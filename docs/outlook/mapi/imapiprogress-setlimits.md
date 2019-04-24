---
title: imapi進捗の制限
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339866"
---
# <a name="imapiprogresssetlimits"></a><span data-ttu-id="ccef9-103">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="ccef9-103">IMAPIProgress::SetLimits</span></span>

  
  
<span data-ttu-id="ccef9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccef9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccef9-105">操作内の項目数の下限と上限を設定します。また、操作の進行状況に関する情報の計算方法を制御するフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="ccef9-105">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ccef9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ccef9-106">Parameters</span></span>

 <span data-ttu-id="ccef9-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="ccef9-107">_lpulMin_</span></span>
  
> <span data-ttu-id="ccef9-108">順番操作中のアイテムの下限を含む変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ccef9-108">[in] A pointer to a variable that contains the lower limit of items in the operation.</span></span>
    
 <span data-ttu-id="ccef9-109">_lプル最大_</span><span class="sxs-lookup"><span data-stu-id="ccef9-109">_lpulMax_</span></span>
  
> <span data-ttu-id="ccef9-110">順番操作中のアイテムの上限を含む変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ccef9-110">[in] A pointer to a variable that contains the upper limit of items in the operation.</span></span>
    
 <span data-ttu-id="ccef9-111">_lアウトフラグ_</span><span class="sxs-lookup"><span data-stu-id="ccef9-111">_lpulFlags_</span></span>
  
> <span data-ttu-id="ccef9-112">順番進行状況情報を計算する操作のレベルを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ccef9-112">[in] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="ccef9-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ccef9-113">The following flag can be set:</span></span>
    
<span data-ttu-id="ccef9-114">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="ccef9-114">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="ccef9-115">imapiprogress の値を使用し[ます。:P rogvalumethod](imapiprogress-progress.md)の_ulcount_および_ulcount_パラメーターは、現在処理されているアイテムとアイテムの合計数を示す、それぞれの処理の進行をインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="ccef9-115">Uses the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters, which indicate the currently processed item and the total items, respectively, to increment progress on the operation.</span></span> <span data-ttu-id="ccef9-116">このフラグが設定されている場合は、グローバルな下限と上限の値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ccef9-116">When this flag is set, the values of the global lower and upper limits have to be set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ccef9-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="ccef9-117">Return value</span></span>

<span data-ttu-id="ccef9-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ccef9-118">S_OK</span></span> 
  
> <span data-ttu-id="ccef9-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="ccef9-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ccef9-120">解説</span><span class="sxs-lookup"><span data-stu-id="ccef9-120">Remarks</span></span>

<span data-ttu-id="ccef9-121">サービスプロバイダーは、 **imapiprogress:: setlimits**メソッドを呼び出して、MAPI_TOP_LEVEL フラグを設定またはクリアし、ローカルおよびグローバルの最小値と最大値を設定します。</span><span class="sxs-lookup"><span data-stu-id="ccef9-121">Service providers call the **IMAPIProgress::SetLimits** method to set or clear the MAPI_TOP_LEVEL flag and to set local and global minimum and maximum values.</span></span> <span data-ttu-id="ccef9-122">flag 設定の値は、progress オブジェクトが最小値と最大値をローカルまたはグローバルに認識するかどうかに影響します。</span><span class="sxs-lookup"><span data-stu-id="ccef9-122">The value of the flag setting affects whether the progress object understands the minimum and maximum values to be local or global.</span></span> <span data-ttu-id="ccef9-123">MAPI_TOP_LEVEL フラグが設定されている場合、これらの値はグローバルと見なされ、操作全体の進行状況を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ccef9-123">When the MAPI_TOP_LEVEL flag is set, these values are considered global and are used to calculate progress for the entire operation.</span></span> <span data-ttu-id="ccef9-124">Progress オブジェクトは、グローバルの最小値を1に、グローバルの最大値を1000に初期化します。</span><span class="sxs-lookup"><span data-stu-id="ccef9-124">Progress objects initialize the global minimum value to 1 and the global maximum value to 1000.</span></span> 
  
<span data-ttu-id="ccef9-125">MAPI_TOP_LEVEL が設定されていない場合、最小値と最大値はローカルと見なされ、プロバイダーはこれらを内部的に使用して、下位レベルのサブオブジェクトの進行状況を表示します。</span><span class="sxs-lookup"><span data-stu-id="ccef9-125">When MAPI_TOP_LEVEL is not set, the minimum and maximum values are considered local, and providers use them internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="ccef9-126">progress オブジェクトは、 [imapiprogress:: getmin](imapiprogress-getmin.md)および[imapiprogress:: getmin](imapiprogress-getmax.md)メソッドが呼び出されたときに、プロバイダーに返されることができるように、ローカルの最小値と最大値のみを保存します。</span><span class="sxs-lookup"><span data-stu-id="ccef9-126">Progress objects save the local minimum and maximum values only so that they can be returned to providers when the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods are called.</span></span> 
  
<span data-ttu-id="ccef9-127">**setlimits**およびその他の[imapiprogress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、「[進行状況インジケーターの実装](implementing-a-progress-indicator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ccef9-127">For more information about how to implement **SetLimits** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="ccef9-128">進行状況オブジェクトを呼び出す方法とタイミングの詳細については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ccef9-128">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ccef9-129">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="ccef9-129">MFCMAPI reference</span></span>

<span data-ttu-id="ccef9-130">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ccef9-130">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ccef9-131">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="ccef9-131">**File**</span></span>|<span data-ttu-id="ccef9-132">**関数**</span><span class="sxs-lookup"><span data-stu-id="ccef9-132">**Function**</span></span>|<span data-ttu-id="ccef9-133">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ccef9-133">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ccef9-134">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="ccef9-134">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="ccef9-135">cmapiprogress 進行状況:: setlimits</span><span class="sxs-lookup"><span data-stu-id="ccef9-135">CMAPIProgress::SetLimits</span></span>  <br/> |<span data-ttu-id="ccef9-136">mfcmapi は、 **imapiprogress:: setlimits**メソッドを使用して、progress オブジェクトの最大値と最小値、およびフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="ccef9-136">MFCMAPI uses the **IMAPIProgress::SetLimits** method to set the maximum and minimum limits and flags for the progress object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccef9-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="ccef9-137">See also</span></span>



[<span data-ttu-id="ccef9-138">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="ccef9-138">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="ccef9-139">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="ccef9-139">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="ccef9-140">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="ccef9-140">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="ccef9-141">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ccef9-141">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="ccef9-142">コード サンプルとしての MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ccef9-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="ccef9-143">進行状況インジケーターを表示する</span><span class="sxs-lookup"><span data-stu-id="ccef9-143">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="ccef9-144">進行状況インジケーターの実装</span><span class="sxs-lookup"><span data-stu-id="ccef9-144">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

