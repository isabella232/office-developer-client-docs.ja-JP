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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9a6ab96a70bce622f44de6576e7b77861302de4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800505"
---
# <a name="imapiformshutdownform"></a><span data-ttu-id="f666b-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="f666b-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="f666b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f666b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f666b-105">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f666b-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="f666b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f666b-106">Parameters</span></span>

 <span data-ttu-id="f666b-107">_ulSaveOptions_</span><span class="sxs-lookup"><span data-stu-id="f666b-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="f666b-108">[in]フォームを閉じる前にフォーム内のデータを保存するかどうか方法を制御する値です。</span><span class="sxs-lookup"><span data-stu-id="f666b-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="f666b-109">次のフラグのいずれかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f666b-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="f666b-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="f666b-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="f666b-111">フォーム データを保存することがありませんか。</span><span class="sxs-lookup"><span data-stu-id="f666b-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="f666b-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="f666b-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="f666b-113">ユーザーは、フォーム内で変更されたデータを保存する求められます。</span><span class="sxs-lookup"><span data-stu-id="f666b-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="f666b-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="f666b-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="f666b-115">最後の保存以降変更されている場合、フォーム データを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f666b-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="f666b-116">ユーザー インターフェイスが表示されていない場合は、フォームを SAVEOPTS_NOSAVE オプションの機能を使用して切り替えることができますオプションで。</span><span class="sxs-lookup"><span data-stu-id="f666b-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f666b-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f666b-117">Return value</span></span>

<span data-ttu-id="f666b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f666b-118">S_OK</span></span> 
  
> <span data-ttu-id="f666b-119">フォームが閉じられました。</span><span class="sxs-lookup"><span data-stu-id="f666b-119">The form was closed.</span></span>
    
<span data-ttu-id="f666b-120">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="f666b-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="f666b-121">**ShutdownForm**の前回の呼び出しで、フォームが既に閉じました。</span><span class="sxs-lookup"><span data-stu-id="f666b-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f666b-122">注釈</span><span class="sxs-lookup"><span data-stu-id="f666b-122">Remarks</span></span>

<span data-ttu-id="f666b-123">フォームの閲覧者は、フォームを終了するのには**IMAPIForm::ShutdownForm**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f666b-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f666b-124">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="f666b-124">Notes to implementers</span></span>

<span data-ttu-id="f666b-125">**ShutdownForm**の実装では、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="f666b-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="f666b-126">確認しているビューアーが既に呼び出されません**ShutdownForm**とがある場合は E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="f666b-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="f666b-127">ではありませんが、チェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f666b-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="f666b-128">処理が完了するまで、フォームと内部データ構造体のストレージが利用可能なままにするために、フォームの[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f666b-128">Call your form's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="f666b-129">フォームのデータに未保存の変更があるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f666b-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="f666b-130">ビューアーの[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)メソッドを呼び出すことによって、 _ulSaveOptions_パラメーターを設定する方法に応じて、保存されていないデータを保存します。</span><span class="sxs-lookup"><span data-stu-id="f666b-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="f666b-131">フォームのユーザー インターフェイスのウィンドウを破棄します。</span><span class="sxs-lookup"><span data-stu-id="f666b-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="f666b-132">[](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出すことによって、フォームのメッセージとメッセージのサイト オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="f666b-132">Release your form's message and message site objects by calling their [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="f666b-133">[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)メソッドを呼び出すことによって登録されているすべての視聴者の保留中のシャット ダウンを通知します。</span><span class="sxs-lookup"><span data-stu-id="f666b-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="f666b-134">アドバイズ シンク ポインターを**null**に設定して、フォームの登録をキャンセルする[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f666b-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="f666b-135">フォームのプロパティのメモリを解放する[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f666b-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="f666b-136">手順 2 で行われた**AddRef**呼び出しに一致するフォームの**** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f666b-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="f666b-137">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="f666b-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="f666b-138">これらの操作を完了すると、呼び出される form オブジェクトにのみ有効なメソッドは、 [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)インターフェイスから。</span><span class="sxs-lookup"><span data-stu-id="f666b-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f666b-139">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f666b-139">Notes to callers</span></span>

<span data-ttu-id="f666b-140">**ShutdownForm**制御が戻るとき、エラーを返すかどうかに関係なく、**リ ス**のメソッドを呼び出して、フォームを離します。</span><span class="sxs-lookup"><span data-stu-id="f666b-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="f666b-141">**ShutdownForm**によって返されるエラーを無視できます。</span><span class="sxs-lookup"><span data-stu-id="f666b-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f666b-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="f666b-142">See also</span></span>



[<span data-ttu-id="f666b-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="f666b-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="f666b-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="f666b-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="f666b-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f666b-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="f666b-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f666b-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f666b-147">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f666b-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

