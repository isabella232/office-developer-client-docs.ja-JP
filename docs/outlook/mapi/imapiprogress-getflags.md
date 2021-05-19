---
title: IMAPIProgressGetFlags
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
# <a name="imapiprogressgetflags"></a><span data-ttu-id="d2df9-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="d2df9-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="d2df9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2df9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2df9-105">進行状況の情報を計算する操作レベルの進行状況オブジェクトからフラグ設定を返します。</span><span class="sxs-lookup"><span data-stu-id="d2df9-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d2df9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d2df9-106">Parameters</span></span>

 <span data-ttu-id="d2df9-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="d2df9-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="d2df9-108">[out]進行状況情報を計算する操作のレベルを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="d2df9-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="d2df9-109">次のフラグを返します。</span><span class="sxs-lookup"><span data-stu-id="d2df9-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="d2df9-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="d2df9-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="d2df9-111">処理を開始するためにクライアントによって呼び出されるオブジェクトである、トップ レベル のオブジェクトの進行状況が計算されています。</span><span class="sxs-lookup"><span data-stu-id="d2df9-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="d2df9-112">たとえば、フォルダー コピー操作のトップ レベル のオブジェクトは、コピーするフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="d2df9-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="d2df9-113">このMAPI_TOP_LEVEL設定されていない場合、下位レベルのオブジェクトまたはサブオブジェクトの進行状況が計算されます。</span><span class="sxs-lookup"><span data-stu-id="d2df9-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="d2df9-114">フォルダー コピー操作では、下位レベルのオブジェクトは、コピーするフォルダー内のサブフォルダーの 1 つになります。</span><span class="sxs-lookup"><span data-stu-id="d2df9-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d2df9-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="d2df9-115">Return value</span></span>

<span data-ttu-id="d2df9-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2df9-116">S_OK</span></span> 
  
> <span data-ttu-id="d2df9-117">flags 値が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="d2df9-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2df9-118">注釈</span><span class="sxs-lookup"><span data-stu-id="d2df9-118">Remarks</span></span>

<span data-ttu-id="d2df9-119">MAPI を使用すると、サービス プロバイダーは、MAPI_TOP_LEVEL フラグを使用してトップ レベル のオブジェクトとサブオブジェクトを区別し、操作に関係するすべてのオブジェクトが同じ [IMAPIProgress](imapiprogressiunknown.md) 実装を使用して進行状況を表示できます。</span><span class="sxs-lookup"><span data-stu-id="d2df9-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="d2df9-120">これにより、インジケーターの表示が 1 つの正の方向にスムーズに進みます。</span><span class="sxs-lookup"><span data-stu-id="d2df9-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="d2df9-121">MAPI_TOP_LEVEL フラグを設定するかどうかは、サービス プロバイダーが後続の progress オブジェクトへの呼び出しで他のパラメーターを設定する方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="d2df9-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="d2df9-122">**GetFlags** によって返される値は、最初は実装者によって設定され、その後 [、IMAPIProgress::SetLimits](imapiprogress-setlimits.md)メソッドへの呼び出しを通じてサービス プロバイダーによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="d2df9-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d2df9-123">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="d2df9-123">Notes to implementers</span></span>

<span data-ttu-id="d2df9-124">常にフラグを初期化してMAPI_TOP_LEVEL、必要に応じてクリアするためにサービス プロバイダーに依存します。</span><span class="sxs-lookup"><span data-stu-id="d2df9-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="d2df9-125">サービス プロバイダーは **、IMAPIProgress::SetLimits** メソッドを呼び出すことによってフラグをクリアおよびリセットできます。</span><span class="sxs-lookup"><span data-stu-id="d2df9-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="d2df9-126">**GetFlags** および他の **IMAPIProgress** メソッドを実装する方法の詳細については、「Progress Indicator の実装 [」を参照してください](implementing-a-progress-indicator.md)。</span><span class="sxs-lookup"><span data-stu-id="d2df9-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="d2df9-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d2df9-127">Notes to callers</span></span>

<span data-ttu-id="d2df9-128">進行状況インジケーターを表示するときに、最初に **IMAPIProgress::GetFlags** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d2df9-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="d2df9-129">すべての実装が  _lpulFlags_ パラメーターの内容をこの値に初期化MAPI_TOP_LEVEL、返される値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2df9-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="d2df9-130">progress オブジェクトへの呼び出しのシーケンスの詳細については、「進捗インジケーターを表示 [する」を参照してください](how-to-display-a-progress-indicator.md)。</span><span class="sxs-lookup"><span data-stu-id="d2df9-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d2df9-131">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="d2df9-131">MFCMAPI reference</span></span>

<span data-ttu-id="d2df9-132">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2df9-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d2df9-133">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="d2df9-133">**File**</span></span>|<span data-ttu-id="d2df9-134">**関数**</span><span class="sxs-lookup"><span data-stu-id="d2df9-134">**Function**</span></span>|<span data-ttu-id="d2df9-135">**コメント**</span><span class="sxs-lookup"><span data-stu-id="d2df9-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d2df9-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="d2df9-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="d2df9-137">CMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="d2df9-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="d2df9-138">MFCMAPI は **IMAPIProgress::GetFlags** メソッドを使用して、設定されているフラグを決定します。</span><span class="sxs-lookup"><span data-stu-id="d2df9-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="d2df9-139">**IMAPIProgress::SetLimits** メソッドを使用してフラグが設定されていないMAPI_TOP_LEVELを返します。</span><span class="sxs-lookup"><span data-stu-id="d2df9-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2df9-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2df9-140">See also</span></span>



[<span data-ttu-id="d2df9-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="d2df9-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="d2df9-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2df9-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="d2df9-143">コード サンプルとしての MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d2df9-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d2df9-144">進行状況インジケーターを表示する</span><span class="sxs-lookup"><span data-stu-id="d2df9-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="d2df9-145">進行状況インジケーターの実装</span><span class="sxs-lookup"><span data-stu-id="d2df9-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

