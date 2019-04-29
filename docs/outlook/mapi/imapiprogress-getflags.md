---
title: imapi進捗 getflags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423644"
---
# <a name="imapiprogressgetflags"></a><span data-ttu-id="99b1f-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="99b1f-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="99b1f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99b1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99b1f-105">進行状況の情報を計算する操作のレベルについて、progress オブジェクトからフラグ設定を返します。</span><span class="sxs-lookup"><span data-stu-id="99b1f-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="99b1f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="99b1f-106">Parameters</span></span>

 <span data-ttu-id="99b1f-107">_lアウトフラグ_</span><span class="sxs-lookup"><span data-stu-id="99b1f-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="99b1f-108">読み上げ進行状況情報を計算する操作のレベルを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="99b1f-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="99b1f-109">次のフラグを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="99b1f-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="99b1f-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="99b1f-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="99b1f-111">処理を開始するためにクライアントによって呼び出されるオブジェクトの最上位レベルのオブジェクトの進行状況が計算されています。</span><span class="sxs-lookup"><span data-stu-id="99b1f-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="99b1f-112">たとえば、フォルダーコピー操作の最上位のオブジェクトは、コピーされているフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="99b1f-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="99b1f-113">MAPI_TOP_LEVEL が設定されていない場合は、下位レベルのオブジェクトまたはサブオブジェクトの進行状況が計算されます。</span><span class="sxs-lookup"><span data-stu-id="99b1f-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="99b1f-114">フォルダーのコピー操作では、下位レベルのオブジェクトは、コピーされているフォルダー内のサブフォルダーの1つです。</span><span class="sxs-lookup"><span data-stu-id="99b1f-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="99b1f-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="99b1f-115">Return value</span></span>

<span data-ttu-id="99b1f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="99b1f-116">S_OK</span></span> 
  
> <span data-ttu-id="99b1f-117">フラグの値が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="99b1f-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99b1f-118">注釈</span><span class="sxs-lookup"><span data-stu-id="99b1f-118">Remarks</span></span>

<span data-ttu-id="99b1f-119">MAPI を使用すると、MAPI_TOP_LEVEL フラグを使用して、処理に関与するすべてのオブジェクトが同じ[imapiprogress](imapiprogressiunknown.md)実装を使用して進行状況を示すことができるように、サービスプロバイダーがトップレベルのオブジェクトとサブオブジェクトを区別できるようになります。</span><span class="sxs-lookup"><span data-stu-id="99b1f-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="99b1f-120">これにより、インジケーター表示が単一の正方向にスムーズに進みます。</span><span class="sxs-lookup"><span data-stu-id="99b1f-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="99b1f-121">MAPI_TOP_LEVEL フラグが設定されているかどうかによって、サービスプロバイダーが以降の呼び出しで progress オブジェクトに対して他のパラメーターを設定する方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="99b1f-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="99b1f-122">**getflags**によって返される値は、最初は実装者によって設定され、その後、 [imapiprogress:: setlimits](imapiprogress-setlimits.md)メソッドを呼び出してサービスプロバイダーによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="99b1f-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="99b1f-123">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="99b1f-123">Notes to implementers</span></span>

<span data-ttu-id="99b1f-124">常にフラグを MAPI_TOP_LEVEL に初期化してから、必要に応じてサービスプロバイダーにクリアするようにします。</span><span class="sxs-lookup"><span data-stu-id="99b1f-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="99b1f-125">サービスプロバイダーは、 **imapiprogress:: setlimits**メソッドを呼び出して、フラグをクリアおよびリセットできます。</span><span class="sxs-lookup"><span data-stu-id="99b1f-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="99b1f-126">**getflags**およびその他の**imapiprogress**メソッドを実装する方法の詳細については、「[進行状況インジケーターの実装](implementing-a-progress-indicator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99b1f-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="99b1f-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="99b1f-127">Notes to callers</span></span>

<span data-ttu-id="99b1f-128">進行状況インジケーターを表示する場合は、最初に**imapiprogress:: getflags**への呼び出しを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="99b1f-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="99b1f-129">すべての実装は、 _lMAPI_TOP_LEVEL flags_パラメーターの内容をこの値に初期化するため、戻り値はである必要があります。</span><span class="sxs-lookup"><span data-stu-id="99b1f-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="99b1f-130">progress オブジェクトへの一連の呼び出しの詳細については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99b1f-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="99b1f-131">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="99b1f-131">MFCMAPI reference</span></span>

<span data-ttu-id="99b1f-132">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99b1f-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="99b1f-133">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="99b1f-133">**File**</span></span>|<span data-ttu-id="99b1f-134">**関数**</span><span class="sxs-lookup"><span data-stu-id="99b1f-134">**Function**</span></span>|<span data-ttu-id="99b1f-135">**コメント**</span><span class="sxs-lookup"><span data-stu-id="99b1f-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99b1f-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="99b1f-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="99b1f-137">cmapiprogress 進行状況:: getflags</span><span class="sxs-lookup"><span data-stu-id="99b1f-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="99b1f-138">mfcmapi は、 **imapiprogress:: getflags**メソッドを使用して、どのフラグが設定されているかを判別します。</span><span class="sxs-lookup"><span data-stu-id="99b1f-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="99b1f-139">**imapiprogress:: setlimits**メソッドを使用してフラグが設定されていない限り、MAPI_TOP_LEVEL を返します。</span><span class="sxs-lookup"><span data-stu-id="99b1f-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99b1f-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="99b1f-140">See also</span></span>



[<span data-ttu-id="99b1f-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="99b1f-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="99b1f-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="99b1f-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="99b1f-143">コード サンプルとしての MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="99b1f-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="99b1f-144">進行状況インジケーターを表示する</span><span class="sxs-lookup"><span data-stu-id="99b1f-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="99b1f-145">進行状況インジケーターの実装</span><span class="sxs-lookup"><span data-stu-id="99b1f-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

