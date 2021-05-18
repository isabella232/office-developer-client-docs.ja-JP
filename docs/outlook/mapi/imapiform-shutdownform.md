---
title: IMAPIFormShutdownForm
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
# <a name="imapiformshutdownform"></a><span data-ttu-id="84a9d-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="84a9d-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="84a9d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84a9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84a9d-105">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="84a9d-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="84a9d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a9d-106">Parameters</span></span>

 <span data-ttu-id="84a9d-107">_ulSaveOptions_</span><span class="sxs-lookup"><span data-stu-id="84a9d-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="84a9d-108">[in]フォームを閉じる前に、フォーム内のデータを保存する方法またはかどうかを制御する値。</span><span class="sxs-lookup"><span data-stu-id="84a9d-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="84a9d-109">次のいずれかのフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="84a9d-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="84a9d-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="84a9d-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="84a9d-111">フォーム データを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84a9d-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="84a9d-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="84a9d-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="84a9d-113">ユーザーは、フォームに変更されたデータを保存するように求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="84a9d-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="84a9d-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="84a9d-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="84a9d-115">フォーム データは、前回の保存以降に変更された場合に保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84a9d-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="84a9d-116">ユーザー インターフェイスが表示されない場合は、必要に応じてフォームを [ユーザー インターフェイス] オプションの機能を使用SAVEOPTS_NOSAVEできます。</span><span class="sxs-lookup"><span data-stu-id="84a9d-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84a9d-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="84a9d-117">Return value</span></span>

<span data-ttu-id="84a9d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="84a9d-118">S_OK</span></span> 
  
> <span data-ttu-id="84a9d-119">フォームが閉じられました。</span><span class="sxs-lookup"><span data-stu-id="84a9d-119">The form was closed.</span></span>
    
<span data-ttu-id="84a9d-120">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="84a9d-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="84a9d-121">このフォームは、ShutdownForm の事前呼び出しによって既 **に閉じられました**。</span><span class="sxs-lookup"><span data-stu-id="84a9d-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="84a9d-122">注釈</span><span class="sxs-lookup"><span data-stu-id="84a9d-122">Remarks</span></span>

<span data-ttu-id="84a9d-123">フォーム ビューアーは **IMAPIForm::ShutdownForm** メソッドを呼び出してフォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="84a9d-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="84a9d-124">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="84a9d-124">Notes to implementers</span></span>

<span data-ttu-id="84a9d-125">ShutdownForm の実装で次のタスク **を実行します**。</span><span class="sxs-lookup"><span data-stu-id="84a9d-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="84a9d-126">ビューアーが **ShutdownForm** をまだ呼び出していないか確認し、存在する場合E_UNEXPECTEDを返します。</span><span class="sxs-lookup"><span data-stu-id="84a9d-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="84a9d-127">これはありそうもないが、確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84a9d-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="84a9d-128">フォームの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) メソッドを呼び出して、フォームのストレージと内部データ構造を処理が完了するまで使用できます。</span><span class="sxs-lookup"><span data-stu-id="84a9d-128">Call your form's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="84a9d-129">フォームのデータに保存されていない変更が含されているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="84a9d-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="84a9d-130">ビューアーの [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)メソッドを呼び出して _、ulSaveOptions_ パラメーターの設定方法に従って、保存されていないデータを保存します。</span><span class="sxs-lookup"><span data-stu-id="84a9d-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="84a9d-131">フォームのユーザー インターフェイス ウィンドウを破棄します。</span><span class="sxs-lookup"><span data-stu-id="84a9d-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="84a9d-132">フォームのメッセージおよびメッセージ サイト オブジェクトを [解放するには、IUnknown::Release メソッドを呼び](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) 出します。</span><span class="sxs-lookup"><span data-stu-id="84a9d-132">Release your form's message and message site objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="84a9d-133">[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)メソッドを呼び出して、保留中のシャットダウンを登録しているすべてのビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="84a9d-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="84a9d-134">[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出して、アドバイス シンク ポインターを null に設定して、通知のためにフォームの登録をキャンセル **します**。</span><span class="sxs-lookup"><span data-stu-id="84a9d-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="84a9d-135">[MAPIFreeBuffer 関数を呼](mapifreebuffer.md)び出して、フォームのプロパティのメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="84a9d-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="84a9d-136">手順 2 で行った **AddRef** 呼び出しと一致する、フォームの **IUnknown::Release** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="84a9d-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="84a9d-137">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="84a9d-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="84a9d-138">これらのアクションが完了すると、呼び出される可能性があるフォーム オブジェクトの有効なメソッドは [、IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) インターフェイスからのメソッドのみです。</span><span class="sxs-lookup"><span data-stu-id="84a9d-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="84a9d-139">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="84a9d-139">Notes to callers</span></span>

<span data-ttu-id="84a9d-140">**ShutdownForm が** 返された場合、エラーが返されるかどうかに関係なく **、IUnknown::Release** メソッドを呼び出してフォームを解放します。</span><span class="sxs-lookup"><span data-stu-id="84a9d-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="84a9d-141">ShutdownForm によって返されるエラーは無視しても **問題ない**。</span><span class="sxs-lookup"><span data-stu-id="84a9d-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="84a9d-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="84a9d-142">See also</span></span>



[<span data-ttu-id="84a9d-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="84a9d-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="84a9d-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="84a9d-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="84a9d-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="84a9d-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="84a9d-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="84a9d-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="84a9d-147">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="84a9d-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

