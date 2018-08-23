---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 15e2d5c2aca595c3a06d215cd069c23da3e48125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800620"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="1527c-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="1527c-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="1527c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1527c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1527c-105">オフライン オブジェクトをオンラインまたはオフラインの現在の状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="1527c-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="1527c-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="1527c-106">Parameters</span></span>

 <span data-ttu-id="1527c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1527c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1527c-108">[in]この呼び出しの動作を変更します。</span><span class="sxs-lookup"><span data-stu-id="1527c-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="1527c-109">サポートされている値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1527c-109">The supported values are:</span></span>
    
<span data-ttu-id="1527c-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="1527c-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="1527c-111">_UlFlags_をこの値に設定する場合は、状態の変更が完了するまで、 **SetCurrentState**の呼び出しがブロックされます。</span><span class="sxs-lookup"><span data-stu-id="1527c-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="1527c-112">トランジションは、既定で非同期的に配置します。</span><span class="sxs-lookup"><span data-stu-id="1527c-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="1527c-113">移行は、非同期的に発生している、 **SetCurrentState**のすべての呼び出しは、変更が完了するまでには**E_PENDING**を返します。</span><span class="sxs-lookup"><span data-stu-id="1527c-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="1527c-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="1527c-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="1527c-115">ブロックすることがなく現在の状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="1527c-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="1527c-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="1527c-116">_ulMask_</span></span>
  
> <span data-ttu-id="1527c-117">[in]変更の状態の一部です。</span><span class="sxs-lookup"><span data-stu-id="1527c-117">[in] The part of the state to change.</span></span> <span data-ttu-id="1527c-118">唯一のサポートされている値は、MAPIOFFLINE_STATE_OFFLINE_MASK です。</span><span class="sxs-lookup"><span data-stu-id="1527c-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="1527c-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="1527c-119">_ulState_</span></span>
  
> <span data-ttu-id="1527c-120">[in]状態に変更します。</span><span class="sxs-lookup"><span data-stu-id="1527c-120">[in] The state to change to.</span></span> <span data-ttu-id="1527c-121">これら 2 つの値のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1527c-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="1527c-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="1527c-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="1527c-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="1527c-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="1527c-124">_保持_</span><span class="sxs-lookup"><span data-stu-id="1527c-124">_pReserved_</span></span>
  
> <span data-ttu-id="1527c-125">このパラメーターは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1527c-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1527c-126">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1527c-126">Return value</span></span>

<span data-ttu-id="1527c-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="1527c-127">S_OK</span></span>
  
> <span data-ttu-id="1527c-128">オフラインのオブジェクトの状態が正常に変更されました。</span><span class="sxs-lookup"><span data-stu-id="1527c-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="1527c-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="1527c-129">E_PENDING</span></span>
  
> <span data-ttu-id="1527c-130">これは、オフラインのオブジェクトの状態が非同期的に変化していることを示します。</span><span class="sxs-lookup"><span data-stu-id="1527c-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="1527c-131">_UlFlags_は、呼び出しでは、以前**SetCurrentState** MAPIOFFLINE_FLAG_BLOCK に設定されており、非同期状態の変更が完了するまで、後続の**SetCurrentState**呼び出しでこの値を返すが場合です。</span><span class="sxs-lookup"><span data-stu-id="1527c-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1527c-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="1527c-132">See also</span></span>



[<span data-ttu-id="1527c-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="1527c-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="1527c-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="1527c-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="1527c-135">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="1527c-135">MAPI Constants</span></span>](mapi-constants.md)

