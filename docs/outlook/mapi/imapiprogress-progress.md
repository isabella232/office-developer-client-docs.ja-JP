---
title: IMAPIProgressProgress
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
# <a name="imapiprogressprogress"></a><span data-ttu-id="e8f20-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="e8f20-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="e8f20-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8f20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8f20-105">進行状況インジケーターを更新し、操作の完了に向けて進行状況を表示します。</span><span class="sxs-lookup"><span data-stu-id="e8f20-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="e8f20-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e8f20-106">Parameters</span></span>

 <span data-ttu-id="e8f20-107">_ulValue_</span><span class="sxs-lookup"><span data-stu-id="e8f20-107">_ulValue_</span></span>
  
> <span data-ttu-id="e8f20-108">[in]グローバル下限とグローバル上限の間の現在の進行状況レベル _(ulCount_ パラメーターと _ulTotal_ パラメーター、[または IMAPIProgress::SetLimits](imapiprogress-setlimits.md)メソッドの _lpulMin_ パラメーターおよび _lpulMax_ パラメーターから計算) を示す数値。</span><span class="sxs-lookup"><span data-stu-id="e8f20-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="e8f20-109">_ulCount_</span><span class="sxs-lookup"><span data-stu-id="e8f20-109">_ulCount_</span></span>
  
> <span data-ttu-id="e8f20-110">[in]合計を基準に現在処理されているアイテムを示す数値。</span><span class="sxs-lookup"><span data-stu-id="e8f20-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="e8f20-111">_ulTotal_</span><span class="sxs-lookup"><span data-stu-id="e8f20-111">_ulTotal_</span></span>
  
> <span data-ttu-id="e8f20-112">[in]操作中に処理されるアイテムの総数。</span><span class="sxs-lookup"><span data-stu-id="e8f20-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e8f20-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="e8f20-113">Return value</span></span>

<span data-ttu-id="e8f20-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8f20-114">S_OK</span></span> 
  
> <span data-ttu-id="e8f20-115">進行状況インジケーターが正常に更新されました。</span><span class="sxs-lookup"><span data-stu-id="e8f20-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="e8f20-116">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="e8f20-116">Notes to implementers</span></span>

<span data-ttu-id="e8f20-117">_ulValue_ パラメーターは、操作の開始時点でのみグローバル最小値、および操作の完了時にのみグローバル最大値に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="e8f20-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="e8f20-118">_ulCount パラメーターと_ _ulTotal_ パラメーター (使用可能な場合) を使用して、オプションのメッセージ ("10 から 5 アイテムが完了しました" など) を表示します。</span><span class="sxs-lookup"><span data-stu-id="e8f20-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="e8f20-119">_ulCount と_ _ulTotal_ が 0 に設定されている場合は、進行状況インジケーターを視覚的に変更するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e8f20-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="e8f20-120">一部のサービス プロバイダーは、親オブジェクトに対して進行状況を監視するサブオブジェクトを処理している場合に、これらのパラメーターを 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="e8f20-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="e8f20-121">このような場合は、親オブジェクトが進行状況を報告した場合にのみ表示を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8f20-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="e8f20-122">一部のサービス プロバイダーは、これらのパラメーターに対して毎回 0 を渡します。</span><span class="sxs-lookup"><span data-stu-id="e8f20-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="e8f20-123">**Progress** および他の [IMAPIProgress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、「Progress Indicator の実装 [」を参照してください](implementing-a-progress-indicator.md)。</span><span class="sxs-lookup"><span data-stu-id="e8f20-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e8f20-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e8f20-124">Notes to callers</span></span>

<span data-ttu-id="e8f20-125">**IMAPIProgress::P 3** つのパラメーターすべてが必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="e8f20-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="e8f20-126">必要なパラメーターは  _ulValue_ のみで、進行状況の割合を示す数値です。</span><span class="sxs-lookup"><span data-stu-id="e8f20-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="e8f20-127">このフラグMAPI_TOP_LEVEL設定されている場合は、オブジェクト数とオブジェクトの合計を渡す方法も指定できます。</span><span class="sxs-lookup"><span data-stu-id="e8f20-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="e8f20-128">一部の実装では、これらの値を使用して、進行状況インジケーターと一緒に "10 から 5 アイテムが完了しました" などの語句を表示します。</span><span class="sxs-lookup"><span data-stu-id="e8f20-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="e8f20-129">1 つのフォルダー内のすべてのメッセージをコピーする場合は  _、ulTotal_ をコピーするメッセージの総数に設定します。</span><span class="sxs-lookup"><span data-stu-id="e8f20-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="e8f20-130">フォルダーをコピーする場合は、フォルダー内のサブフォルダーの数に  _ulTotal_ を設定します。</span><span class="sxs-lookup"><span data-stu-id="e8f20-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="e8f20-131">コピーするフォルダーにサブフォルダーとメッセージだけが含まれている場合は  _、ulTotal を_ 1 に設定します。</span><span class="sxs-lookup"><span data-stu-id="e8f20-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="e8f20-132">進行状況オブジェクトを呼び出す方法とタイミングの詳細については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8f20-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e8f20-133">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="e8f20-133">MFCMAPI reference</span></span>

<span data-ttu-id="e8f20-134">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8f20-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e8f20-135">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="e8f20-135">**File**</span></span>|<span data-ttu-id="e8f20-136">**関数**</span><span class="sxs-lookup"><span data-stu-id="e8f20-136">**Function**</span></span>|<span data-ttu-id="e8f20-137">**コメント**</span><span class="sxs-lookup"><span data-stu-id="e8f20-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e8f20-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="e8f20-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="e8f20-139">CMAPIProgress::P rogress</span><span class="sxs-lookup"><span data-stu-id="e8f20-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="e8f20-140">MFCMAPI は **IMAPIProgress::P rogress** メソッドを使用して  _、uValue_ および現在の最大値と最小値から計算された現在の進捗率で MFCMAPI ステータス バーを更新します。</span><span class="sxs-lookup"><span data-stu-id="e8f20-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8f20-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8f20-141">See also</span></span>



[<span data-ttu-id="e8f20-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="e8f20-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="e8f20-143">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e8f20-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="e8f20-144">コード サンプルとしての MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e8f20-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="e8f20-145">進行状況インジケーターを表示する</span><span class="sxs-lookup"><span data-stu-id="e8f20-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="e8f20-146">進行状況インジケーターの実装</span><span class="sxs-lookup"><span data-stu-id="e8f20-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

