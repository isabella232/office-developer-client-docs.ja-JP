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
# <a name="imapicontrolgetstate"></a><span data-ttu-id="502a6-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="502a6-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="502a6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="502a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="502a6-105">ボタン コントロールが有効か無効かを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="502a6-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="502a6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="502a6-106">Parameters</span></span>

 <span data-ttu-id="502a6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="502a6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="502a6-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="502a6-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="502a6-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="502a6-109">_lpulState_</span></span>
  
> <span data-ttu-id="502a6-110">[out]ボタン コントロールの状態を示す値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="502a6-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="502a6-111">次のいずれかの値を返します。</span><span class="sxs-lookup"><span data-stu-id="502a6-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="502a6-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="502a6-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="502a6-113">ボタン コントロールは無効になり、クリックできません。</span><span class="sxs-lookup"><span data-stu-id="502a6-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="502a6-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="502a6-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="502a6-115">ボタン コントロールが有効で、クリックできます。</span><span class="sxs-lookup"><span data-stu-id="502a6-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="502a6-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="502a6-116">Return value</span></span>

<span data-ttu-id="502a6-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="502a6-117">S_OK</span></span> 
  
> <span data-ttu-id="502a6-118">ボタン コントロールの状態が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="502a6-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="502a6-119">注釈</span><span class="sxs-lookup"><span data-stu-id="502a6-119">Remarks</span></span>

<span data-ttu-id="502a6-120">サービス プロバイダーは **、IMAPIControl::GetState** メソッドを実装して、MAPI にボタン コントロールの状態を提供します。</span><span class="sxs-lookup"><span data-stu-id="502a6-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="502a6-121">ボタンが有効になっている場合は、マウスのクリックまたはキーを押す操作に応答できます。</span><span class="sxs-lookup"><span data-stu-id="502a6-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="502a6-122">無効にすると、ボタンが淡色表示になり、マウスのクリックやキーの押しに応答しません。</span><span class="sxs-lookup"><span data-stu-id="502a6-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="502a6-123">**GetState** および他の [IMAPIControl : IUnknown](imapicontroliunknown.md)メソッドを実装する方法の詳細については [、「Control Object Implementation 」を参照してください](control-object-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="502a6-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="502a6-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="502a6-124">See also</span></span>



[<span data-ttu-id="502a6-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="502a6-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="502a6-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="502a6-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

