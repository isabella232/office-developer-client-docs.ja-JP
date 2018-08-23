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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a5e4205a808c7a6e469d2e9cb0a1b3c17a92d21
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573545"
---
# <a name="imapiprogressgetflags"></a><span data-ttu-id="b185f-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="b185f-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="b185f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b185f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b185f-105">返します。 操作の進行状況に関する情報は、計算対象のレベルに進行中のオブジェクトから設定にフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="b185f-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b185f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b185f-106">Parameters</span></span>

 <span data-ttu-id="b185f-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="b185f-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="b185f-108">[out]進捗状況の情報を計算する操作のレベルを制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="b185f-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="b185f-109">次のフラグを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="b185f-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="b185f-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="b185f-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="b185f-111">進行状況は、最上位レベルのオブジェクトでは、操作を開始するクライアントによって呼び出されるオブジェクトの中に計算されます。</span><span class="sxs-lookup"><span data-stu-id="b185f-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="b185f-112">たとえば、フォルダーのコピー操作で最上位レベルのオブジェクトは、コピーされているフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="b185f-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="b185f-113">MAPI_TOP_LEVEL が設定されていない場合は、下位レベルのオブジェクトまたはサブオブジェクトの進行状況が計算されます。</span><span class="sxs-lookup"><span data-stu-id="b185f-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="b185f-114">フォルダーのコピー操作では下位レベルのオブジェクトがコピーされているフォルダー内のサブフォルダーのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="b185f-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b185f-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b185f-115">Return value</span></span>

<span data-ttu-id="b185f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b185f-116">S_OK</span></span> 
  
> <span data-ttu-id="b185f-117">フラグの値が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="b185f-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b185f-118">注釈</span><span class="sxs-lookup"><span data-stu-id="b185f-118">Remarks</span></span>

<span data-ttu-id="b185f-119">MAPI 最上位のオブジェクトを区別するためにサービス プロバイダーを有効にし、MAPI_TOP_LEVEL フラグを使用してサブオブジェクト操作ですべてのオブジェクトが含まれるように実装を使用できます同じ[IMAPIProgress](imapiprogressiunknown.md)の進行状況を表示します。</span><span class="sxs-lookup"><span data-stu-id="b185f-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="b185f-120">インジケーターの表示をスムーズに進むと 1 つの正の方向に発生します。</span><span class="sxs-lookup"><span data-stu-id="b185f-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="b185f-121">MAPI_TOP_LEVEL フラグが設定されているかどうかは、サービス プロバイダーが実行中のオブジェクトへの以降の呼び出しで他のパラメーターを設定する方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="b185f-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="b185f-122">**GetFlags**によって返される値は実装によって、後で[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)メソッドを呼び出すことによってサービス ・ プロバイダーによって最初に設定します。</span><span class="sxs-lookup"><span data-stu-id="b185f-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b185f-123">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="b185f-123">Notes to implementers</span></span>

<span data-ttu-id="b185f-124">常に MAPI_TOP_LEVEL フラグの内容を初期化しをオフにするときは、適切なサービス プロバイダーに任せることです。</span><span class="sxs-lookup"><span data-stu-id="b185f-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="b185f-125">サービス プロバイダーでは、オフにでき、 **IMAPIProgress::SetLimits**メソッドを呼び出すことによって、フラグをリセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="b185f-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="b185f-126">**GetFlags**およびその他の**IMAPIProgress**メソッドを実装する方法の詳細については、[進行状況のインジケーターを実装する](implementing-a-progress-indicator.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b185f-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b185f-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b185f-127">Notes to callers</span></span>

<span data-ttu-id="b185f-128">進行状況のインジケーターを表示する場合は、最初の呼び出しは、 **IMAPIProgress::GetFlags**呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="b185f-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="b185f-129">返された値は、すべての実装がこの値を_lpulFlags_パラメーターの内容を初期化するため、MAPI_TOP_LEVEL にすることがあります。</span><span class="sxs-lookup"><span data-stu-id="b185f-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="b185f-130">進行中のオブジェクトへの呼び出しのシーケンスの詳細については、[進行状況のインジケーターの表示](how-to-display-a-progress-indicator.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b185f-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b185f-131">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="b185f-131">MFCMAPI reference</span></span>

<span data-ttu-id="b185f-132">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="b185f-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b185f-133">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="b185f-133">**File**</span></span>|<span data-ttu-id="b185f-134">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="b185f-134">**Function**</span></span>|<span data-ttu-id="b185f-135">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="b185f-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b185f-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="b185f-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="b185f-137">CMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="b185f-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="b185f-138">MFCMAPI では、 **IMAPIProgress::GetFlags**メソッドを使用して、どのフラグが設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="b185f-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="b185f-139">**IMAPIProgress::SetLimits**メソッドを使用して、フラグが設定されていない限り、MAPI_TOP_LEVEL を返します。</span><span class="sxs-lookup"><span data-stu-id="b185f-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b185f-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="b185f-140">See also</span></span>



[<span data-ttu-id="b185f-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="b185f-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="b185f-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b185f-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


<span data-ttu-id="b185f-143">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b185f-143">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="b185f-144">進行状況インジケーターを表示する</span><span class="sxs-lookup"><span data-stu-id="b185f-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="b185f-145">進行状況インジケーターの実装</span><span class="sxs-lookup"><span data-stu-id="b185f-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

