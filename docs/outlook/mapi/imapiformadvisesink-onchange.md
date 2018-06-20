---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 01bdf6cdde864d1ea4ed19dfeb01a96236dc9c63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800514"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="f9367-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="f9367-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="f9367-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f9367-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f9367-105">フォーム ビューアーのステータスに変更が発生したことを示します。</span><span class="sxs-lookup"><span data-stu-id="f9367-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="f9367-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f9367-106">Parameters</span></span>

 <span data-ttu-id="f9367-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="f9367-107">_ulDir_</span></span>
  
> <span data-ttu-id="f9367-108">[in]ビューアーと、フォーム内の予想される応答で発生した変更に関する情報を提供するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="f9367-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="f9367-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f9367-109">The following flags can be set:</span></span>
    
<span data-ttu-id="f9367-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="f9367-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="f9367-111">別のカテゴリで次または前のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9367-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="f9367-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="f9367-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="f9367-113">フォームは、ユーザー インターフェイスを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9367-113">The form should display a user interface.</span></span> <span data-ttu-id="f9367-114">このフラグが設定されていない場合、フォームが動詞が表示されるユーザー インターフェイスは、通常原因への応答であっても、ユーザー インターフェイスを表示するを抑制する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9367-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="f9367-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="f9367-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="f9367-116">フォームがモーダル フォーム ビューアーに表示します。</span><span class="sxs-lookup"><span data-stu-id="f9367-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="f9367-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="f9367-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="f9367-118">フォーム ビューアーに次のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9367-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="f9367-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="f9367-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="f9367-120">フォーム ビューアーで前のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9367-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="f9367-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="f9367-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="f9367-122">削除、送信、および移動の操作を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9367-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="f9367-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="f9367-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="f9367-124">フォーム ビューアーで次または前の未読メ ッ セージがあります。</span><span class="sxs-lookup"><span data-stu-id="f9367-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f9367-125">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f9367-125">Return value</span></span>

<span data-ttu-id="f9367-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9367-126">S_OK</span></span> 
  
> <span data-ttu-id="f9367-127">通知が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="f9367-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9367-128">備考</span><span class="sxs-lookup"><span data-stu-id="f9367-128">Remarks</span></span>

<span data-ttu-id="f9367-129">フォーム ビューアーは、ビューアーのステータスの変更のフォームを通知するために**IMAPIFormAdviseSink::OnChange**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f9367-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="f9367-130">通常、唯一の変更は設定か、ビューアー内の次または前のメッセージの有無に基づいて、VCSTATUS_NEXT または VCSTATUS_PREVIOUS フラグをオフにします。</span><span class="sxs-lookup"><span data-stu-id="f9367-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="f9367-131">したがって、フォーム オブジェクトは、有効または、サポートする前または次のアクションを無効にします。</span><span class="sxs-lookup"><span data-stu-id="f9367-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="f9367-132">VCSTATUS_MODAL と VCSTATUS_INTERACTIVE の設定は、それが作成された後、ビューのコンテキストで変更できません。</span><span class="sxs-lookup"><span data-stu-id="f9367-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f9367-133">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="f9367-133">Notes to implementers</span></span>

<span data-ttu-id="f9367-134">このメソッドの特定の実装では、フォームの仕様に完全に依存しています。</span><span class="sxs-lookup"><span data-stu-id="f9367-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="f9367-135">フォームのほとんどのオブジェクトは、独自のユーザー インターフェイス (たとえば、有効にするか、ビューアーのステータス フラグのパラメーターと一致するのにには、メニュー コマンドやボタンを無効にするのに場合など) を変更するのにはこのメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f9367-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f9367-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="f9367-136">See also</span></span>



[<span data-ttu-id="f9367-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="f9367-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="f9367-138">IMAPIFormAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f9367-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

