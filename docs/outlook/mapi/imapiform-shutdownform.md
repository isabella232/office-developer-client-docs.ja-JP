---
title: imapiformshutdownform
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 073a76766a296d86e7a23809921b832d494a8f1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329478"
---
# <a name="imapiformshutdownform"></a><span data-ttu-id="d537c-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="d537c-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="d537c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d537c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d537c-105">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d537c-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="d537c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d537c-106">Parameters</span></span>

 <span data-ttu-id="d537c-107">_ulsaveoptions_</span><span class="sxs-lookup"><span data-stu-id="d537c-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="d537c-108">順番フォームを閉じる前に、フォーム内のデータを保存するかどうかを制御する値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d537c-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="d537c-109">次のいずれかのフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d537c-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="d537c-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="d537c-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="d537c-111">フォームデータは保存しないようにします。</span><span class="sxs-lookup"><span data-stu-id="d537c-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="d537c-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="d537c-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="d537c-113">ユーザーは、変更されたデータをフォームに保存するかどうかを確認するメッセージを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d537c-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="d537c-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="d537c-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="d537c-115">前回の保存以降に変更されている場合は、フォームデータを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d537c-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="d537c-116">ユーザーインターフェイスが表示されていない場合は、必要に応じて、SAVEOPTS_NOSAVE オプションの機能を使用してフォームを切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="d537c-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d537c-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="d537c-117">Return value</span></span>

<span data-ttu-id="d537c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d537c-118">S_OK</span></span> 
  
> <span data-ttu-id="d537c-119">フォームが閉じられました。</span><span class="sxs-lookup"><span data-stu-id="d537c-119">The form was closed.</span></span>
    
<span data-ttu-id="d537c-120">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="d537c-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="d537c-121">このフォームは、以前に**shutdownform**を呼び出したときに既に閉じられています。</span><span class="sxs-lookup"><span data-stu-id="d537c-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d537c-122">解説</span><span class="sxs-lookup"><span data-stu-id="d537c-122">Remarks</span></span>

<span data-ttu-id="d537c-123">フォームビューアーは、 **imapiform:: shutdownform**メソッドを呼び出してフォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d537c-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d537c-124">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="d537c-124">Notes to implementers</span></span>

<span data-ttu-id="d537c-125">**shutdownform**の実装で、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="d537c-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="d537c-126">viewer が**shutdownform**を呼び出していないことを確認し、E_UNEXPECTED がある場合はそれを返します。</span><span class="sxs-lookup"><span data-stu-id="d537c-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="d537c-127">このことはほとんどありませんが、確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d537c-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="d537c-128">フォームの[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)メソッドを呼び出して、フォームおよび内部データ構造のストレージを処理が完了するまで引き続き使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d537c-128">Call your form's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="d537c-129">フォームのデータに保存されていない変更があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="d537c-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="d537c-130">[IMAPIMessageSite:: SaveMessage](imapimessagesite-savemessage.md)メソッドを呼び出すことにより、 _ulsaveoptions_パラメーターの設定方法に従って未保存のデータを保存します。</span><span class="sxs-lookup"><span data-stu-id="d537c-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="d537c-131">フォームのユーザーインターフェイスウィンドウを破棄します。</span><span class="sxs-lookup"><span data-stu-id="d537c-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="d537c-132">[IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出して、フォームのメッセージおよびメッセージサイトオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="d537c-132">Release your form's message and message site objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="d537c-133">[IMAPIViewAdviseSink:: onshutdown](imapiviewadvisesink-onshutdown.md)メソッドを呼び出して、保留中のシャットダウンのすべての登録済みビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="d537c-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="d537c-134">[imapiviewcontext:: SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出して、アドバイズシンクポインターを**null**に設定することにより、フォームの通知の登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="d537c-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="d537c-135">[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、フォームのプロパティのメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="d537c-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="d537c-136">手順2で作成した**AddRef**呼び出しに一致するように、フォームの**IUnknown:: Release**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d537c-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="d537c-137">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="d537c-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="d537c-138">これらの操作が完了した後、呼び出される可能性のある form オブジェクトの有効なメソッドは、 [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)インターフェイスからのものだけです。</span><span class="sxs-lookup"><span data-stu-id="d537c-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d537c-139">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d537c-139">Notes to callers</span></span>

<span data-ttu-id="d537c-140">エラーが返されるかどうかに関係なく、 **shutdownform**から制御が戻ると、 **IUnknown:: release**メソッドを呼び出してフォームを解放します。</span><span class="sxs-lookup"><span data-stu-id="d537c-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="d537c-141">**shutdownform**によって返されるエラーは無視しても問題ありません。</span><span class="sxs-lookup"><span data-stu-id="d537c-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d537c-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="d537c-142">See also</span></span>



[<span data-ttu-id="d537c-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="d537c-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="d537c-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="d537c-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="d537c-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d537c-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="d537c-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d537c-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d537c-147">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d537c-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

