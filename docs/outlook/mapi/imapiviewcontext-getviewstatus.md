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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429018"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="941c0-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="941c0-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="941c0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="941c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="941c0-105">現在のビューアーの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="941c0-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="941c0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="941c0-106">Parameters</span></span>

 <span data-ttu-id="941c0-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="941c0-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="941c0-108">[out]ビューアーの状態を提供するフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="941c0-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="941c0-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="941c0-109">The following flags can be set:</span></span>
    
<span data-ttu-id="941c0-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="941c0-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="941c0-111">別のカテゴリに次または前のメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="941c0-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="941c0-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="941c0-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="941c0-113">フォームを使用すると、メッセージを削除できます。</span><span class="sxs-lookup"><span data-stu-id="941c0-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="941c0-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="941c0-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="941c0-115">フォームにユーザー インターフェイスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="941c0-115">The form should display a user interface.</span></span> <span data-ttu-id="941c0-116">このフラグを設定しない場合、フォームは、通常はユーザー インターフェイスが表示される動詞に応答しても、ユーザー インターフェイスの表示を抑制する必要があります。</span><span class="sxs-lookup"><span data-stu-id="941c0-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="941c0-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="941c0-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="941c0-118">フォームはビューアーに対してモーダルです。</span><span class="sxs-lookup"><span data-stu-id="941c0-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="941c0-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="941c0-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="941c0-120">ビューに次のメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="941c0-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="941c0-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="941c0-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="941c0-122">ビューに前のメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="941c0-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="941c0-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="941c0-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="941c0-124">メッセージは読み取り専用モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="941c0-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="941c0-125">削除、送信、および移動操作は無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="941c0-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="941c0-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="941c0-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="941c0-127">ビューに次または前の未読メッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="941c0-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="941c0-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="941c0-128">Return value</span></span>

<span data-ttu-id="941c0-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="941c0-129">S_OK</span></span> 
  
> <span data-ttu-id="941c0-130">ビューアーの状態が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="941c0-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="941c0-131">注釈</span><span class="sxs-lookup"><span data-stu-id="941c0-131">Remarks</span></span>

<span data-ttu-id="941c0-132">フォーム オブジェクトは **IMAPIViewContext::GetViewStatus** メソッドを呼び出して、次のコマンドがメッセージをアクティブ化する方向、前のコマンドがメッセージをアクティブ化する方向、または両方向で、フォーム ビューでアクティブ化するメッセージが増えるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="941c0-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="941c0-133">_lpulStatus_ パラメーターが示す値を使用して [、imapIViewContext::ActivateNext](imapiviewcontext-activatenext.md)に対して VCSTATUS_NEXT フラグと VCSTATUS_PREV フラグが有効かどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="941c0-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="941c0-134">VCSTATUS_DELETE フラグが設定されているが、VCSTATUS_READONLY フラグが設定されていない場合は [、IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) メソッドを使用してメッセージを削除できます。</span><span class="sxs-lookup"><span data-stu-id="941c0-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="941c0-135">通常、フォームは、ビューアーのコンテキストに対して無効な場合、メニュー コマンドとボタンを無効にします。</span><span class="sxs-lookup"><span data-stu-id="941c0-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="941c0-136">閲覧者は [、IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) メソッドを呼び出すことによって、フォームに状態の変更を通知できます。</span><span class="sxs-lookup"><span data-stu-id="941c0-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="941c0-137">フォームVCSTATUS_MODAL前の [IMAPIForm::D oVerb](imapiform-doverb.md) 呼び出しでハンドルが渡されるウィンドウにモーダルである必要がある場合、このフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="941c0-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="941c0-138">このVCSTATUS_MODAL設定されている場合、フォームは、フォームが閉じるまで **DoVerb** 呼び出しが行われたスレッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="941c0-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="941c0-139">このVCSTATUS_MODAL設定されていない場合、フォームはこのウィンドウにモーダルではなく、スレッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="941c0-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="941c0-140">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="941c0-140">MFCMAPI reference</span></span>

<span data-ttu-id="941c0-141">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="941c0-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="941c0-142">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="941c0-142">**File**</span></span>|<span data-ttu-id="941c0-143">**関数**</span><span class="sxs-lookup"><span data-stu-id="941c0-143">**Function**</span></span>|<span data-ttu-id="941c0-144">**コメント**</span><span class="sxs-lookup"><span data-stu-id="941c0-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="941c0-145">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="941c0-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="941c0-146">CMyMAPIFormViewer::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="941c0-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="941c0-147">MFCMAPI は、 **この関数に IMAPIViewContext::GetViewStatus** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="941c0-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="941c0-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="941c0-148">See also</span></span>



[<span data-ttu-id="941c0-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="941c0-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="941c0-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="941c0-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


<span data-ttu-id="941c0-151">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="941c0-151">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

