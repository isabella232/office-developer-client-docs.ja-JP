---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fb543f4188578483333614cb5768f903c9f243d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800901"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="0f18d-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="0f18d-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="0f18d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f18d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f18d-105">ビューアーの現在の状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f18d-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="0f18d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f18d-106">Parameters</span></span>

 <span data-ttu-id="0f18d-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="0f18d-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="0f18d-108">[out]ビュアーのステータスを提供するフラグのビットマップへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f18d-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="0f18d-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="0f18d-109">The following flags can be set:</span></span>
    
<span data-ttu-id="0f18d-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="0f18d-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="0f18d-111">別のカテゴリで次または前のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0f18d-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="0f18d-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="0f18d-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="0f18d-113">フォームにより、メッセージが削除されます。</span><span class="sxs-lookup"><span data-stu-id="0f18d-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="0f18d-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="0f18d-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="0f18d-115">フォームは、ユーザー インターフェイスを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f18d-115">The form should display a user interface.</span></span> <span data-ttu-id="0f18d-116">このフラグが設定されていない場合は、フォームがユーザー インターフェイスを表示するのには通常、動詞への応答であっても、ユーザー インターフェイスを表示するを抑制する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f18d-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="0f18d-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="0f18d-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="0f18d-118">フォームでは、ビューアーに固有の値です。</span><span class="sxs-lookup"><span data-stu-id="0f18d-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="0f18d-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="0f18d-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="0f18d-120">ビューで次のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0f18d-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="0f18d-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="0f18d-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="0f18d-122">ビューで前のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0f18d-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="0f18d-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="0f18d-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="0f18d-124">メッセージでは、読み取り専用モードで開くことができません。</span><span class="sxs-lookup"><span data-stu-id="0f18d-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="0f18d-125">削除、送信、および移動の操作を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f18d-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="0f18d-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="0f18d-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="0f18d-127">ビューで次または前の未読メ ッ セージがあります。</span><span class="sxs-lookup"><span data-stu-id="0f18d-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0f18d-128">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0f18d-128">Return value</span></span>

<span data-ttu-id="0f18d-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f18d-129">S_OK</span></span> 
  
> <span data-ttu-id="0f18d-130">ビューアーのステータスが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="0f18d-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f18d-131">注釈</span><span class="sxs-lookup"><span data-stu-id="0f18d-131">Remarks</span></span>

<span data-ttu-id="0f18d-132">フォーム オブジェクトのいずれかのフォーム ビューでアクティブにするより多くのメッセージがあるかどうかを決定する**IMAPIViewContext::GetViewStatus**メソッドを呼び出して、または双方向は、**次**のコマンドをアクティブにする方向でのメッセージで、**前**のコマンドが、メッセージをアクティブにする方向または双方向にします。</span><span class="sxs-lookup"><span data-stu-id="0f18d-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="0f18d-133">VCSTATUS_NEXT と VCSTATUS_PREV のフラグが[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)に対して有効かどうかを確認するのには、 _lpulStatus_パラメーターが指す値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0f18d-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="0f18d-134">フラグの場合、VCSTATUS_DELETE セットがない、VCSTATUS_READONLY フラグは、 [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md)メソッドを使用してメッセージを削除することができますし。</span><span class="sxs-lookup"><span data-stu-id="0f18d-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="0f18d-135">通常、フォームを無効にするメニュー コマンドやボタンのコンテキストに対して有効でない場合。</span><span class="sxs-lookup"><span data-stu-id="0f18d-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="0f18d-136">ビューアーは、その[IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md)メソッドを呼び出して、ステータスの変更をするためのフォームを警告できます。</span><span class="sxs-lookup"><span data-stu-id="0f18d-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="0f18d-137">フォームをモーダル ウィンドウのハンドルが渡される必要がある場合、VCSTATUS_MODAL フラグが設定されて、以前の[IMAPIForm::DoVerb](imapiform-doverb.md)呼び出しで。</span><span class="sxs-lookup"><span data-stu-id="0f18d-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="0f18d-138">VCSTATUS_MODAL が設定されている場合、フォームは、フォームを閉じるまでの**DoVerb**呼び出しを行ったスレッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0f18d-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="0f18d-139">VCSTATUS_MODAL が設定されていない場合、フォームはモーダル ウィンドウにすることはできず、スレッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f18d-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0f18d-140">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="0f18d-140">MFCMAPI reference</span></span>

<span data-ttu-id="0f18d-141">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="0f18d-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0f18d-142">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="0f18d-142">**File**</span></span>|<span data-ttu-id="0f18d-143">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="0f18d-143">**Function**</span></span>|<span data-ttu-id="0f18d-144">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="0f18d-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0f18d-145">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="0f18d-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="0f18d-146">CMyMAPIFormViewer::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="0f18d-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="0f18d-147">MFCMAPI では、この関数では、 **IMAPIViewContext::GetViewStatus**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="0f18d-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0f18d-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f18d-148">See also</span></span>



[<span data-ttu-id="0f18d-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="0f18d-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="0f18d-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0f18d-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


<span data-ttu-id="0f18d-151">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="0f18d-151">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

