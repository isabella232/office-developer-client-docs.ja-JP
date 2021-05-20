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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 02663570e3173bbd696af732e71f060d9dee49bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431898"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="ced70-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="ced70-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="ced70-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ced70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ced70-105">フォーム ビューアーの状態で変更が発生したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ced70-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="ced70-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ced70-106">Parameters</span></span>

 <span data-ttu-id="ced70-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="ced70-107">_ulDir_</span></span>
  
> <span data-ttu-id="ced70-108">[in]ビューアーで発生した変更とフォームの予想される応答に関する情報を提供するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ced70-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="ced70-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ced70-109">The following flags can be set:</span></span>
    
<span data-ttu-id="ced70-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="ced70-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="ced70-111">別のカテゴリに次または前のメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="ced70-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="ced70-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="ced70-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="ced70-113">フォームにユーザー インターフェイスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ced70-113">The form should display a user interface.</span></span> <span data-ttu-id="ced70-114">このフラグを設定しない場合、フォームは、通常はユーザー インターフェイスが表示される動詞に応答しても、ユーザー インターフェイスの表示を抑制する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ced70-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="ced70-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="ced70-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="ced70-116">フォームは、フォーム ビューアーに対してモーダルになる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ced70-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="ced70-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="ced70-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="ced70-118">フォーム ビューアーに次のメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="ced70-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="ced70-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="ced70-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="ced70-120">フォーム ビューアーに前のメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="ced70-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="ced70-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="ced70-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="ced70-122">削除、送信、および移動操作は無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ced70-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="ced70-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="ced70-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="ced70-124">フォーム ビューアーに次または前の未読メッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="ced70-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ced70-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="ced70-125">Return value</span></span>

<span data-ttu-id="ced70-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="ced70-126">S_OK</span></span> 
  
> <span data-ttu-id="ced70-127">通知が成功しました。</span><span class="sxs-lookup"><span data-stu-id="ced70-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ced70-128">注釈</span><span class="sxs-lookup"><span data-stu-id="ced70-128">Remarks</span></span>

<span data-ttu-id="ced70-129">フォーム ビューアーは **IMAPIFormAdviseSink::OnChange** メソッドを呼び出して、ビューアーの状態の変更についてフォームに通知します。</span><span class="sxs-lookup"><span data-stu-id="ced70-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="ced70-130">通常、変更は、ビューアー内の次VCSTATUS_NEXTまたはVCSTATUS_PREVIOUSメッセージの有無に基づいて、VCSTATUS_NEXT または VCSTATUS_PREVIOUS フラグを設定またはクリアするのみです。</span><span class="sxs-lookup"><span data-stu-id="ced70-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="ced70-131">したがって、フォーム オブジェクトは、サポートする次または以前のアクションを有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="ced70-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="ced70-132">ビュー コンテキストのVCSTATUS_MODAL設定VCSTATUS_INTERACTIVE作成後は、ビュー コンテキストで変更できません。</span><span class="sxs-lookup"><span data-stu-id="ced70-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ced70-133">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="ced70-133">Notes to implementers</span></span>

<span data-ttu-id="ced70-134">このメソッドの具体的な実装は、フォームの詳細に完全に依存します。</span><span class="sxs-lookup"><span data-stu-id="ced70-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="ced70-135">ほとんどのフォーム オブジェクトは、このメソッドを使用してユーザー インターフェイスを変更します (たとえば、ビューアーの状態フラグ パラメーターに一致するメニュー コマンドやボタンを有効または無効にします)。</span><span class="sxs-lookup"><span data-stu-id="ced70-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ced70-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="ced70-136">See also</span></span>



[<span data-ttu-id="ced70-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ced70-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="ced70-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ced70-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

