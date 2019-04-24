---
title: imapiviewcontextgetviewstatus
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
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351178"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="fc775-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="fc775-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="fc775-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc775-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc775-105">現在のビューアーの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="fc775-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="fc775-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fc775-106">Parameters</span></span>

 <span data-ttu-id="fc775-107">_lアウト状態_</span><span class="sxs-lookup"><span data-stu-id="fc775-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="fc775-108">読み上げビューアーの状態を提供するフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fc775-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="fc775-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="fc775-109">The following flags can be set:</span></span>
    
<span data-ttu-id="fc775-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="fc775-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="fc775-111">別のカテゴリに、次または前のメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="fc775-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="fc775-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="fc775-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="fc775-113">フォームでは、メッセージを削除できます。</span><span class="sxs-lookup"><span data-stu-id="fc775-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="fc775-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="fc775-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="fc775-115">フォームにユーザーインターフェイスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc775-115">The form should display a user interface.</span></span> <span data-ttu-id="fc775-116">このフラグが設定されていない場合、通常はユーザーインターフェイスが表示される原因となる動詞に応答しても、フォームはユーザーインターフェイスを表示しません。</span><span class="sxs-lookup"><span data-stu-id="fc775-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="fc775-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="fc775-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="fc775-118">フォームはビューアーに対してモーダルです。</span><span class="sxs-lookup"><span data-stu-id="fc775-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="fc775-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="fc775-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="fc775-120">ビューに次のメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="fc775-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="fc775-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="fc775-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="fc775-122">ビューに前のメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="fc775-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="fc775-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="fc775-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="fc775-124">メッセージは読み取り専用モードで開かれます。</span><span class="sxs-lookup"><span data-stu-id="fc775-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="fc775-125">Delete、submit、および move 操作を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc775-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="fc775-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="fc775-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="fc775-127">ビューに次または前の未読メッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="fc775-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc775-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="fc775-128">Return value</span></span>

<span data-ttu-id="fc775-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc775-129">S_OK</span></span> 
  
> <span data-ttu-id="fc775-130">閲覧者の状態が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="fc775-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc775-131">解説</span><span class="sxs-lookup"><span data-stu-id="fc775-131">Remarks</span></span>

<span data-ttu-id="fc775-132">form オブジェクトは、 **imapiviewcontext:: getviewstatus**メソッドを呼び出して、**次**のコマンドがメッセージをアクティブ化する方向で、またはその両方の方向に、フォームビューでアクティブ化するメッセージがまだあるかどうかを判断します。**前**のコマンドがメッセージをアクティブにする方向、または両方の方向。</span><span class="sxs-lookup"><span data-stu-id="fc775-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="fc775-133">_lVCSTATUS_NEXT status_パラメーターで指定された値は、VCSTATUS_PREV フラグが[imapiviewcontext:: ActivateNext](imapiviewcontext-activatenext.md)に対して有効かどうかを判断するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fc775-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="fc775-134">VCSTATUS_DELETE フラグが設定されていても、VCSTATUS_READONLY フラグが設定されていない場合は、 [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md)メソッドを使用してメッセージを削除できます。</span><span class="sxs-lookup"><span data-stu-id="fc775-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="fc775-135">通常、フォームはメニューコマンドとボタンが閲覧者のコンテキストに対して有効でない場合は無効にします。</span><span class="sxs-lookup"><span data-stu-id="fc775-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="fc775-136">ビューアーは、 [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md)メソッドを呼び出すことによって、状態を変化させるようにフォームに通知できます。</span><span class="sxs-lookup"><span data-stu-id="fc775-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="fc775-137">VCSTATUS_MODAL フラグが設定されているのは、以前の imapiform でハンドルが渡されているウィンドウに対してフォームがモーダルである必要がある場合です[。:D overb](imapiform-doverb.md)呼び出し。</span><span class="sxs-lookup"><span data-stu-id="fc775-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="fc775-138">VCSTATUS_MODAL が設定されている場合、フォームが閉じるまで、 **DoVerb**呼び出しが行われたスレッドをフォームで使用できます。</span><span class="sxs-lookup"><span data-stu-id="fc775-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="fc775-139">VCSTATUS_MODAL が設定されていない場合、このウィンドウではフォームがモーダルではないので、スレッドを使用してはなりません。</span><span class="sxs-lookup"><span data-stu-id="fc775-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fc775-140">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="fc775-140">MFCMAPI reference</span></span>

<span data-ttu-id="fc775-141">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc775-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fc775-142">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="fc775-142">**File**</span></span>|<span data-ttu-id="fc775-143">**関数**</span><span class="sxs-lookup"><span data-stu-id="fc775-143">**Function**</span></span>|<span data-ttu-id="fc775-144">**コメント**</span><span class="sxs-lookup"><span data-stu-id="fc775-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fc775-145">MyMAPIFormViewer</span><span class="sxs-lookup"><span data-stu-id="fc775-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="fc775-146">cmymapiformviewer:: getviewstatus</span><span class="sxs-lookup"><span data-stu-id="fc775-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="fc775-147">mfcmapi は、この関数の**imapiviewcontext:: getviewstatus**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="fc775-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc775-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc775-148">See also</span></span>



[<span data-ttu-id="fc775-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="fc775-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="fc775-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fc775-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


<span data-ttu-id="fc775-151">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="fc775-151">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

