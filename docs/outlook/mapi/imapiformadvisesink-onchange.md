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
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="2f32d-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="2f32d-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="2f32d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f32d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f32d-105">フォームビューアーの状態で変更が発生したことを示します。</span><span class="sxs-lookup"><span data-stu-id="2f32d-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="2f32d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2f32d-106">Parameters</span></span>

 <span data-ttu-id="2f32d-107">_uldir_</span><span class="sxs-lookup"><span data-stu-id="2f32d-107">_ulDir_</span></span>
  
> <span data-ttu-id="2f32d-108">順番viewer で発生した変更に関する情報と、フォームで想定される応答を提供するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="2f32d-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="2f32d-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2f32d-109">The following flags can be set:</span></span>
    
<span data-ttu-id="2f32d-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="2f32d-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="2f32d-111">別のカテゴリに、次または前のメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="2f32d-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="2f32d-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="2f32d-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="2f32d-113">フォームにユーザーインターフェイスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f32d-113">The form should display a user interface.</span></span> <span data-ttu-id="2f32d-114">このフラグが設定されていない場合、通常、ユーザーインターフェイスが表示される原因となる動詞に応答している場合でも、フォームはユーザーインターフェイスを表示しません。</span><span class="sxs-lookup"><span data-stu-id="2f32d-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="2f32d-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="2f32d-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="2f32d-116">フォームビューアーのモーダルにします。</span><span class="sxs-lookup"><span data-stu-id="2f32d-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="2f32d-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="2f32d-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="2f32d-118">フォームビューアーに次のメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="2f32d-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="2f32d-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="2f32d-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="2f32d-120">フォームビューアーに前のメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="2f32d-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="2f32d-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="2f32d-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="2f32d-122">Delete、submit、および move 操作を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f32d-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="2f32d-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="2f32d-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="2f32d-124">フォームビューアーに、次または前の未読メッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="2f32d-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2f32d-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="2f32d-125">Return value</span></span>

<span data-ttu-id="2f32d-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="2f32d-126">S_OK</span></span> 
  
> <span data-ttu-id="2f32d-127">通知は正常に実行されました。</span><span class="sxs-lookup"><span data-stu-id="2f32d-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2f32d-128">注釈</span><span class="sxs-lookup"><span data-stu-id="2f32d-128">Remarks</span></span>

<span data-ttu-id="2f32d-129">フォームビューアーは**IMAPIFormAdviseSink:: OnChange**メソッドを呼び出して、閲覧者のステータスの変更についてフォームに通知します。</span><span class="sxs-lookup"><span data-stu-id="2f32d-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="2f32d-130">通常、この変更は、閲覧者の次または前のメッセージが存在するかどうかに基づいて、VCSTATUS_NEXT または VCSTATUS_PREVIOUS フラグを設定またはクリアすることだけです。</span><span class="sxs-lookup"><span data-stu-id="2f32d-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="2f32d-131">そのため、form オブジェクトは、サポートする次または前のアクションを有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="2f32d-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="2f32d-132">VCSTATUS_MODAL および VCSTATUS_INTERACTIVE の設定は、作成後にビューコンテキストで変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="2f32d-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2f32d-133">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="2f32d-133">Notes to implementers</span></span>

<span data-ttu-id="2f32d-134">このメソッドの具体的な実装は、フォームの仕様に完全に依存しています。</span><span class="sxs-lookup"><span data-stu-id="2f32d-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="2f32d-135">ほとんどの form オブジェクトは、このメソッドを使用してユーザーインターフェイスを変更します (たとえば、メニューコマンドやボタンを有効または無効にしてビューア状態フラグパラメーターに一致させる)。</span><span class="sxs-lookup"><span data-stu-id="2f32d-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f32d-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f32d-136">See also</span></span>



[<span data-ttu-id="2f32d-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="2f32d-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="2f32d-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2f32d-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

