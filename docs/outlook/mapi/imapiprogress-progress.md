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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2a003be35fc9c3ef8efc7c66997ee99f6e578f09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800640"
---
# <a name="imapiprogressprogress"></a><span data-ttu-id="406be-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="406be-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="406be-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="406be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="406be-105">加えられると、操作の完了までの進捗状況の表示と進行状況のインジケーターが更新されます。</span><span class="sxs-lookup"><span data-stu-id="406be-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="406be-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="406be-106">Parameters</span></span>

 <span data-ttu-id="406be-107">_ulValue_</span><span class="sxs-lookup"><span data-stu-id="406be-107">_ulValue_</span></span>
  
> <span data-ttu-id="406be-108">[in]グローバル間 ( _ulCount_および_ulTotal_パラメーターとは、 _lpulMin_と_lpulMax_メソッドのパラメーター、 [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)から計算) を実行中の現在のレベルを示す数値下限値と上限にはグローバルです。</span><span class="sxs-lookup"><span data-stu-id="406be-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="406be-109">_ulCount_</span><span class="sxs-lookup"><span data-stu-id="406be-109">_ulCount_</span></span>
  
> <span data-ttu-id="406be-110">[in]現在処理されて項目の合計を示す数値です。</span><span class="sxs-lookup"><span data-stu-id="406be-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="406be-111">_ulTotal_</span><span class="sxs-lookup"><span data-stu-id="406be-111">_ulTotal_</span></span>
  
> <span data-ttu-id="406be-112">[in]操作中に処理する品目の合計数です。</span><span class="sxs-lookup"><span data-stu-id="406be-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="406be-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="406be-113">Return value</span></span>

<span data-ttu-id="406be-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="406be-114">S_OK</span></span> 
  
> <span data-ttu-id="406be-115">進行状況インジケーターが正常に更新されました。</span><span class="sxs-lookup"><span data-stu-id="406be-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="406be-116">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="406be-116">Notes to implementers</span></span>

<span data-ttu-id="406be-117">_UlValue_パラメーターは、グローバルの最小値、操作の開始時だけにし、操作の完了時にのみグローバルの最大値に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="406be-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="406be-118">「5 アイテム 10 個が完了した」などのオプションのメッセージを表示するのには、利用可能な場合、 _ulCount_および_ulTotal_パラメーターを使用してください。</span><span class="sxs-lookup"><span data-stu-id="406be-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="406be-119">_UlCount_と_ulTotal_は、0 に設定されている場合は、進行状況を視覚的に変更するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="406be-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="406be-120">サービス プロバイダーによっては、サブオブジェクトの進行状況は、親オブジェクトを基準にして処理することを示すために 0 にこれらのパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="406be-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="406be-121">このような状況は、親オブジェクトの進行状況を報告する場合にのみ、表示を変更します。</span><span class="sxs-lookup"><span data-stu-id="406be-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="406be-122">サービス プロバイダーによっては、毎回これらのパラメーターに 0 を渡します。</span><span class="sxs-lookup"><span data-stu-id="406be-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="406be-123">**進行状況**およびその他の[IMAPIProgress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、[進行状況のインジケーターを実装する](implementing-a-progress-indicator.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="406be-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="406be-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="406be-124">Notes to callers</span></span>

<span data-ttu-id="406be-125">**IMAPIProgress::Progress**のパラメーターのすべての 3 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="406be-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="406be-126">必要な唯一のパラメーターは、 _ulValue_、進行状況の割合を示す数値です。</span><span class="sxs-lookup"><span data-stu-id="406be-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="406be-127">MAPI_TOP_LEVEL フラグが設定されている場合は、オブジェクト数と、オブジェクトの合計も渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="406be-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="406be-128">いくつかの実装では、進行状況インジケーターを 5 アイテム 10 個の完了] などの語句を表示するのにこれらの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="406be-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="406be-129">1 つのフォルダー内のすべてのメッセージをコピーする場合は、コピーされるメッセージの合計数に_ulTotal_を設定します。</span><span class="sxs-lookup"><span data-stu-id="406be-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="406be-130">フォルダーをコピーする場合は、フォルダー内のサブフォルダーの数に_ulTotal_を設定します。</span><span class="sxs-lookup"><span data-stu-id="406be-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="406be-131">コピーするフォルダーが含まれていないメッセージのみのサブフォルダーと、 _ulTotal_が 1 に設定します。</span><span class="sxs-lookup"><span data-stu-id="406be-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="406be-132">方法の詳細については、実行中のオブジェクトへの呼び出しを行う場合は、[進行状況のインジケーターの表示](how-to-display-a-progress-indicator.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="406be-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="406be-133">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="406be-133">MFCMAPI reference</span></span>

<span data-ttu-id="406be-134">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="406be-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="406be-135">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="406be-135">**File**</span></span>|<span data-ttu-id="406be-136">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="406be-136">**Function**</span></span>|<span data-ttu-id="406be-137">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="406be-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="406be-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="406be-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="406be-139">CMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="406be-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="406be-140">MFCMAPI では、 **IMAPIProgress::Progress**メソッドを使用して、 _uValue_と現在の最大値と最小値から計算される、進行中の現在の割合で MFCMAPI ステータス バーを更新します。</span><span class="sxs-lookup"><span data-stu-id="406be-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="406be-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="406be-141">See also</span></span>



[<span data-ttu-id="406be-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="406be-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="406be-143">IMAPIProgress: IUnknown</span><span class="sxs-lookup"><span data-stu-id="406be-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


<span data-ttu-id="406be-144">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="406be-144">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="406be-145">進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="406be-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="406be-146">進行状況のインジケーターを実装します。</span><span class="sxs-lookup"><span data-stu-id="406be-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

