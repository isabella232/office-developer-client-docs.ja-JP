---
title: imapiofflinesetlevel
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0b6837b51b09ecd9a60630c613e1806cb10c1d87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421740"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="ab009-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="ab009-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="ab009-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab009-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab009-105">オフラインオブジェクトの現在の状態をオンラインまたはオフラインに設定します。</span><span class="sxs-lookup"><span data-stu-id="ab009-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="ab009-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ab009-106">Parameters</span></span>

 <span data-ttu-id="ab009-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ab009-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ab009-108">順番この呼び出しの動作を変更します。</span><span class="sxs-lookup"><span data-stu-id="ab009-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="ab009-109">サポートされている値を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ab009-109">The supported values are:</span></span>
    
<span data-ttu-id="ab009-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="ab009-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="ab009-111">_ulflags_をこの値に設定すると\*\*\*\* 、状態の変更が完了するまで setlevelcall がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="ab009-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="ab009-112">既定では、移行は非同期的に行われます。</span><span class="sxs-lookup"><span data-stu-id="ab009-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="ab009-113">遷移が非同期で発生している\*\*\*\* 場合、すべての setcurrentstate 呼び出しは、変更が完了するまで\*\*\*\* を返します。</span><span class="sxs-lookup"><span data-stu-id="ab009-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="ab009-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ab009-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="ab009-115">ブロックせずに現在の状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="ab009-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="ab009-116">_ulmask_</span><span class="sxs-lookup"><span data-stu-id="ab009-116">_ulMask_</span></span>
  
> <span data-ttu-id="ab009-117">順番変更する状態の部分。</span><span class="sxs-lookup"><span data-stu-id="ab009-117">[in] The part of the state to change.</span></span> <span data-ttu-id="ab009-118">サポートされている値は MAPIOFFLINE_STATE_OFFLINE_MASK のみです。</span><span class="sxs-lookup"><span data-stu-id="ab009-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="ab009-119">_ulstate_</span><span class="sxs-lookup"><span data-stu-id="ab009-119">_ulState_</span></span>
  
> <span data-ttu-id="ab009-120">順番変更後の状態。</span><span class="sxs-lookup"><span data-stu-id="ab009-120">[in] The state to change to.</span></span> <span data-ttu-id="ab009-121">次の2つの値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab009-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="ab009-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="ab009-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="ab009-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="ab009-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="ab009-124">_保持され_</span><span class="sxs-lookup"><span data-stu-id="ab009-124">_pReserved_</span></span>
  
> <span data-ttu-id="ab009-125">このパラメーターは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ab009-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ab009-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="ab009-126">Return value</span></span>

<span data-ttu-id="ab009-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab009-127">S_OK</span></span>
  
> <span data-ttu-id="ab009-128">オフラインオブジェクトの状態が正常に変更されました。</span><span class="sxs-lookup"><span data-stu-id="ab009-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="ab009-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="ab009-129">E_PENDING</span></span>
  
> <span data-ttu-id="ab009-130">これは、オフラインオブジェクトの状態が非同期に変化していることを示します。</span><span class="sxs-lookup"><span data-stu-id="ab009-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="ab009-131">これは、 _ulflags_が以前の setcurrentstate に設定\*\*\*\* されている場合に発生し、以降の**setcurrentstate**変更が完了するまでこの値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ab009-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ab009-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab009-132">See also</span></span>



[<span data-ttu-id="ab009-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="ab009-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="ab009-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="ab009-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="ab009-135">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="ab009-135">MAPI Constants</span></span>](mapi-constants.md)

