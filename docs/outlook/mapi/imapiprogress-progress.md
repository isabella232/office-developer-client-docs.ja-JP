---
title: imapi進捗状況
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.Progress
api_type:
- COM
ms.assetid: edbf7623-a64e-43b8-8379-e3cde2433d91
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3cf639286a504b9edb600214d13dbe50710e76a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435496"
---
# <a name="imapiprogressprogress"></a><span data-ttu-id="4641a-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="4641a-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="4641a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4641a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4641a-105">操作が完了した時点で進行状況のインジケーターを更新します。</span><span class="sxs-lookup"><span data-stu-id="4641a-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="4641a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4641a-106">Parameters</span></span>

 <span data-ttu-id="4641a-107">_ulvalue_</span><span class="sxs-lookup"><span data-stu-id="4641a-107">_ulValue_</span></span>
  
> <span data-ttu-id="4641a-108">順番現在の進行状況のレベルを示す数値 ( _ulcount_および_ulcount_パラメーター、または[imapiprogress:: setlimits](imapiprogress-setlimits.md)メソッドの_l/min_および_lアウト max_パラメーターから、グローバルな間で計算されます)。下限とグローバルの上限値。</span><span class="sxs-lookup"><span data-stu-id="4641a-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="4641a-109">_ulcount_</span><span class="sxs-lookup"><span data-stu-id="4641a-109">_ulCount_</span></span>
  
> <span data-ttu-id="4641a-110">順番現在処理されているアイテムを合計に対して示す数値。</span><span class="sxs-lookup"><span data-stu-id="4641a-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="4641a-111">_ultotal_</span><span class="sxs-lookup"><span data-stu-id="4641a-111">_ulTotal_</span></span>
  
> <span data-ttu-id="4641a-112">順番操作中に処理されるアイテムの合計数。</span><span class="sxs-lookup"><span data-stu-id="4641a-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4641a-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="4641a-113">Return value</span></span>

<span data-ttu-id="4641a-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="4641a-114">S_OK</span></span> 
  
> <span data-ttu-id="4641a-115">進行状況のインジケーターが正常に更新されました。</span><span class="sxs-lookup"><span data-stu-id="4641a-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="4641a-116">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="4641a-116">Notes to implementers</span></span>

<span data-ttu-id="4641a-117">_ulvalue_パラメーターは、操作の開始時にのみグローバル最小値となり、操作の完了時にのみグローバル最大値に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="4641a-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="4641a-118">_ulcount_パラメーターと_ulcount_パラメーター (使用可能な場合) を使用して、"5 個のアイテムが完了しました" のようなオプションのメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="4641a-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="4641a-119">_ulcount_と_ulcount_が0に設定されている場合は、進行状況インジケーターを視覚的に変更するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4641a-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="4641a-120">一部のサービスプロバイダーでは、このパラメーターを0に設定して、進行状況が親オブジェクトに対して監視されているサブオブジェクトを処理していることを示します。</span><span class="sxs-lookup"><span data-stu-id="4641a-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="4641a-121">このような状況では、親オブジェクトが進捗状況を報告する場合にのみ、表示を変更することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4641a-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="4641a-122">一部のサービスプロバイダーは、これらのパラメーターに対して常に0を渡します。</span><span class="sxs-lookup"><span data-stu-id="4641a-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="4641a-123">**進行状況**およびその他の[imapiprogress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、「[進行状況インジケーターの実装](implementing-a-progress-indicator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4641a-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4641a-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4641a-124">Notes to callers</span></span>

<span data-ttu-id="4641a-125">**imapiprogress**の3つのパラメーターすべてではありません。:P rogress が必要です。</span><span class="sxs-lookup"><span data-stu-id="4641a-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="4641a-126">必須のパラメーターは_ulvalue_のみで、進行状況の割合を示す数値です。</span><span class="sxs-lookup"><span data-stu-id="4641a-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="4641a-127">MAPI_TOP_LEVEL フラグが設定されている場合は、オブジェクトの数と合計を渡すこともできます。</span><span class="sxs-lookup"><span data-stu-id="4641a-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="4641a-128">実装によっては、これらの値を使用して、進行状況のインジケーターが表示された "5 個のアイテムが10を完了しました" のような語句を表示します。</span><span class="sxs-lookup"><span data-stu-id="4641a-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="4641a-129">すべてのメッセージを単一のフォルダーにコピーする場合は、 _ultotal_をコピーするメッセージの合計数に設定します。</span><span class="sxs-lookup"><span data-stu-id="4641a-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="4641a-130">フォルダーをコピーする場合は、 _ultotal_をフォルダー内のサブフォルダーの数に設定します。</span><span class="sxs-lookup"><span data-stu-id="4641a-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="4641a-131">コピーするフォルダーにサブフォルダーとメッセージのみが含まれている場合は、 _ultotal_を1に設定します。</span><span class="sxs-lookup"><span data-stu-id="4641a-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="4641a-132">進行状況オブジェクトを呼び出す方法とタイミングの詳細については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4641a-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4641a-133">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="4641a-133">MFCMAPI reference</span></span>

<span data-ttu-id="4641a-134">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4641a-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4641a-135">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="4641a-135">**File**</span></span>|<span data-ttu-id="4641a-136">**関数**</span><span class="sxs-lookup"><span data-stu-id="4641a-136">**Function**</span></span>|<span data-ttu-id="4641a-137">**コメント**</span><span class="sxs-lookup"><span data-stu-id="4641a-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4641a-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="4641a-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="4641a-139">cmapiprogress 進行状況::P rogress</span><span class="sxs-lookup"><span data-stu-id="4641a-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="4641a-140">mfcmapi は、 **imapiprogress::P rogvalumethod**を使用して、現在の進行状況 ( _uvalue_および現在の最大値および最小値から計算された) を使用して、mfcmapi ステータスバーを更新します。</span><span class="sxs-lookup"><span data-stu-id="4641a-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4641a-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="4641a-141">See also</span></span>



[<span data-ttu-id="4641a-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="4641a-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="4641a-143">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4641a-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="4641a-144">コード サンプルとしての MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4641a-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="4641a-145">進行状況インジケーターを表示する</span><span class="sxs-lookup"><span data-stu-id="4641a-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="4641a-146">進行状況インジケーターの実装</span><span class="sxs-lookup"><span data-stu-id="4641a-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

