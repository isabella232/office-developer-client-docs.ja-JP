---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f477c617533d66fc129c7192c9f86bb8a46afbb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419010"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="d5af4-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="d5af4-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="d5af4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5af4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5af4-105">ボタンコントロールが有効であるか無効であるかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5af4-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="d5af4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5af4-106">Parameters</span></span>

 <span data-ttu-id="d5af4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d5af4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d5af4-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="d5af4-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d5af4-109">_lアウト状態_</span><span class="sxs-lookup"><span data-stu-id="d5af4-109">_lpulState_</span></span>
  
> <span data-ttu-id="d5af4-110">読み上げボタンコントロールの状態を示す値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5af4-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="d5af4-111">次のいずれかの値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d5af4-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="d5af4-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="d5af4-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="d5af4-113">[ボタン] コントロールは無効になっていて、クリックできません。</span><span class="sxs-lookup"><span data-stu-id="d5af4-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="d5af4-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="d5af4-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="d5af4-115">[ボタン] コントロールが有効になり、クリックできるようになります。</span><span class="sxs-lookup"><span data-stu-id="d5af4-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d5af4-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5af4-116">Return value</span></span>

<span data-ttu-id="d5af4-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5af4-117">S_OK</span></span> 
  
> <span data-ttu-id="d5af4-118">ボタンコントロールの状態が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="d5af4-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5af4-119">注釈</span><span class="sxs-lookup"><span data-stu-id="d5af4-119">Remarks</span></span>

<span data-ttu-id="d5af4-120">サービスプロバイダーは、 **IMAPIControl:: GetState**メソッドを実装して、ボタンコントロールの状態を MAPI に提供します。</span><span class="sxs-lookup"><span data-stu-id="d5af4-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="d5af4-121">ボタンが有効になっている場合は、マウスのクリックまたはキーの押すに応答することができます。</span><span class="sxs-lookup"><span data-stu-id="d5af4-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="d5af4-122">無効にすると、ボタンは淡色表示になり、マウスクリックまたはキーを押しても反応しません。</span><span class="sxs-lookup"><span data-stu-id="d5af4-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="d5af4-123">**GetState**およびその他の[IMAPIControl: IUnknown](imapicontroliunknown.md)メソッドを実装する方法の詳細については、「 [Control オブジェクトの実装](control-object-implementation.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5af4-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5af4-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5af4-124">See also</span></span>



[<span data-ttu-id="d5af4-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="d5af4-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="d5af4-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5af4-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

