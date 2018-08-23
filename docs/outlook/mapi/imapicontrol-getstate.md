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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3d45c4722b6a0200ea3937ba606da0af5c793df2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581854"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="1090a-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="1090a-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="1090a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1090a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1090a-105">ボタン コントロールを有効または無効にするかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="1090a-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="1090a-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="1090a-106">Parameters</span></span>

 <span data-ttu-id="1090a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1090a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1090a-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="1090a-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1090a-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="1090a-109">_lpulState_</span></span>
  
> <span data-ttu-id="1090a-110">[out]ボタン コントロールの状態を示す値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1090a-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="1090a-111">次の値のいずれかが返されます。</span><span class="sxs-lookup"><span data-stu-id="1090a-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="1090a-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="1090a-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="1090a-113">ボタン コントロールは無効になり、クリックすることはできません。</span><span class="sxs-lookup"><span data-stu-id="1090a-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="1090a-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="1090a-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="1090a-115">ボタン コントロールを有効にし、クリックすることができます。</span><span class="sxs-lookup"><span data-stu-id="1090a-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1090a-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1090a-116">Return value</span></span>

<span data-ttu-id="1090a-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="1090a-117">S_OK</span></span> 
  
> <span data-ttu-id="1090a-118">ボタン コントロールの状態が正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="1090a-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1090a-119">注釈</span><span class="sxs-lookup"><span data-stu-id="1090a-119">Remarks</span></span>

<span data-ttu-id="1090a-120">サービス プロバイダーでは、MAPI をボタン コントロールの状態を提供する**IMAPIControl::GetState**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="1090a-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="1090a-121">ボタンが有効の場合は、マウス クリックやキー入力に応答できます。</span><span class="sxs-lookup"><span data-stu-id="1090a-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="1090a-122">無効の場合ボタンは淡色表示とマウス クリックやキー入力に応答しません。</span><span class="sxs-lookup"><span data-stu-id="1090a-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="1090a-123">**GetState**および他の実装方法の詳細については[IMAPIControl: IUnknown](imapicontroliunknown.md)メソッドは、[コントロール オブジェクトの実装](control-object-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1090a-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1090a-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="1090a-124">See also</span></span>



[<span data-ttu-id="1090a-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="1090a-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="1090a-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1090a-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

