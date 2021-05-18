---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 60a8c89afe0d70a1737c6ce694c66359fd6aae4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329462"
---
# <a name="imapiformdoverb"></a><span data-ttu-id="2ab3e-103">IMAPIForm::DoVerb</span><span class="sxs-lookup"><span data-stu-id="2ab3e-103">IMAPIForm::DoVerb</span></span>

  
  
<span data-ttu-id="2ab3e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ab3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ab3e-105">フォームが特定の動詞に関連付けるタスクを実行する要求。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-105">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="2ab3e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2ab3e-106">Parameters</span></span>

 <span data-ttu-id="2ab3e-107">_iVerb_</span><span class="sxs-lookup"><span data-stu-id="2ab3e-107">_iVerb_</span></span>
  
> <span data-ttu-id="2ab3e-108">[in]フォームの動詞の 1 つに関連付けられている番号。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-108">[in] The number associated with one of the form's verbs.</span></span>
    
 <span data-ttu-id="2ab3e-109">_lpViewContext_</span><span class="sxs-lookup"><span data-stu-id="2ab3e-109">_lpViewContext_</span></span>
  
> <span data-ttu-id="2ab3e-110">[in]ビュー コンテキスト オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-110">[in] A pointer to a view context object.</span></span> <span data-ttu-id="2ab3e-111">_lpViewContext パラメーター_ には null を **指定できます**。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-111">The  _lpViewContext_ parameter can be **null**.</span></span>
    
 <span data-ttu-id="2ab3e-112">_hwndParent_</span><span class="sxs-lookup"><span data-stu-id="2ab3e-112">_hwndParent_</span></span>
  
> <span data-ttu-id="2ab3e-113">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-113">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="2ab3e-114">ダイアログ  _ボックスまたはウィンドウが_ モーダルではない場合 **、hwndParent** パラメーターは null である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-114">The  _hwndParent_ parameter should be **null** if the dialog box or window is not modal.</span></span> 
    
 <span data-ttu-id="2ab3e-115">_lprcPosRect_</span><span class="sxs-lookup"><span data-stu-id="2ab3e-115">_lprcPosRect_</span></span>
  
> <span data-ttu-id="2ab3e-116">[in]フォームのウィンドウのサイズと位置を含む Win32 [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-116">[in] A pointer to a Win32 [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the size and position of the form's window.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2ab3e-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="2ab3e-117">Return value</span></span>

<span data-ttu-id="2ab3e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ab3e-118">S_OK</span></span> 
  
> <span data-ttu-id="2ab3e-119">動詞が正常に呼び出されました。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-119">The verb was successfully invoked.</span></span>
    
<span data-ttu-id="2ab3e-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span><span class="sxs-lookup"><span data-stu-id="2ab3e-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span></span> 
  
> <span data-ttu-id="2ab3e-121">_iVerb_ パラメーターで表される動詞は有効ですが、フォームは現在関連付けられている操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-121">The verb represented by the  _iVerb_ parameter is valid, but the form cannot perform the operations currently associated with it.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2ab3e-122">注釈</span><span class="sxs-lookup"><span data-stu-id="2ab3e-122">Remarks</span></span>

<span data-ttu-id="2ab3e-123">フォーム ビューアーは **IMAPIForm::D oVerb** メソッドを呼び出して、フォームがサポートする各動詞に関連付けるタスクをフォームが実行します。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-123">Form viewers call the **IMAPIForm::DoVerb** method to request that the form perform the tasks that it associates with each verb that the form supports.</span></span> 
  
<span data-ttu-id="2ab3e-124">サポートされている各動詞は _、iVerb_ パラメーターで **DoVerb** に渡される数値で識別されます。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-124">Each of the supported verbs is identified by a numeric value, passed to **DoVerb** in the  _iVerb_ parameter.</span></span> <span data-ttu-id="2ab3e-125">DoVerb の一般的な実装には、フォームの **iVerb** パラメーターに対して有効な値をテストする _スイッチ_ ステートメントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-125">Typical implementations of **DoVerb** contain a **switch** statement that tests the values that are valid for the  _iVerb_ parameter for the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2ab3e-126">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="2ab3e-126">Notes to implementers</span></span>

<span data-ttu-id="2ab3e-127">フォーム ビューアーが _lpViewContext_ パラメーターでビュー コンテキストを指定する場合は [、IMAPIForm::SetViewContext](imapiform-setviewcontext.md)メソッドへの以前の呼び出しで渡されたビュー コンテキストではなく **、DoVerb** 実装で使用します。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span></span> <span data-ttu-id="2ab3e-128">内部データ構造に必要な変更を加え、ビュー コンテキストを保存しない。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-128">Make whatever changes are necessary to your internal data structures and do not save the view context.</span></span> 
  
<span data-ttu-id="2ab3e-129">DoVerb 実装で次の **タスクを実行** します。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-129">Perform the following tasks in your **DoVerb** implementation:</span></span> 
  
- <span data-ttu-id="2ab3e-130">_iVerb_ パラメーターに関連付けられている特定の動詞に必要なコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-130">Execute whatever code is necessary for the particular verb that is associated with the  _iVerb_ parameter.</span></span> 
    
- <span data-ttu-id="2ab3e-131">必要に応じて、元のビュー コンテキストを復元します。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-131">If necessary, restore the original view context.</span></span>
    
- <span data-ttu-id="2ab3e-132">不明な動詞番号が渡された場合は、次のMAPI_E_NO_SUPPORT。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-132">If an unknown verb number was passed in, return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="2ab3e-133">それ以外の場合は、実行された動詞の成功または失敗に基づいて結果を返します。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-133">Otherwise, return a result based on the success or failure of whatever verb was executed.</span></span>
    
- <span data-ttu-id="2ab3e-134">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-134">Close the form.</span></span> <span data-ttu-id="2ab3e-135">**DoVerb** 呼び出しの完了後にフォームを閉じるのは常にユーザーの責任です。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-135">It is always your responsibility to close the form after a **DoVerb** call completes.</span></span> 
    
<span data-ttu-id="2ab3e-136">Print などの一部の動詞は **、DoVerb** 呼び出しに関してモーダルである必要があります。つまり **、DoVerb** 呼び出しが返される前に、指定された操作を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-136">Some verbs, such as Print, should be modal with respect to the **DoVerb** call — that is, the indicated operation must be finished before the **DoVerb** call returns.</span></span> 
  
<span data-ttu-id="2ab3e-137">フォームのウィンドウ **で使用される RECT** 構造を取得するには [、GetWindowRect 関数を呼び出](https://msdn.microsoft.com/library/ms633519) します。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-137">To obtain the **RECT** structure used by a form's window, call the [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="2ab3e-138">ハンドルを  _hwndParent_ パラメーターに保存しないのは、通常は **DoVerb** が完了するまで有効なままですが、呼び出しが戻った直後に破棄される可能性があるからです。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-138">Do not save the handle in the  _hwndParent_ parameter because, although it usually remains valid until the completion of **DoVerb**, it can be destroyed immediately upon the call's return.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="2ab3e-139">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2ab3e-139">Notes to callers</span></span>

<span data-ttu-id="2ab3e-140">モーダル以外の動詞をモーダル 動詞として機能させるには [、imapIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)メソッドから VCSTATUS_MODAL フラグを返すビュー コンテキスト実装を _lpViewContext_ をポイントします。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-140">You can make non-modal verbs act as modal verbs by pointing  _lpViewContext_ to a view context implementation that returns the VCSTATUS_MODAL flag from its [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
  
<span data-ttu-id="2ab3e-141">MAPI の動詞の詳細については、「Form [Verbs」を参照してください](form-verbs.md)。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-141">For more information about verbs in MAPI, see [Form Verbs](form-verbs.md).</span></span> <span data-ttu-id="2ab3e-142">OLE での動詞の処理方法の詳細については [、「OLE とデータ転送」を参照してください](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-142">For more information about how verbs are handled in OLE, see [OLE and Data Transfer](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2ab3e-143">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="2ab3e-143">MFCMAPI reference</span></span>

<span data-ttu-id="2ab3e-144">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2ab3e-145">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="2ab3e-145">**File**</span></span>|<span data-ttu-id="2ab3e-146">**関数**</span><span class="sxs-lookup"><span data-stu-id="2ab3e-146">**Function**</span></span>|<span data-ttu-id="2ab3e-147">**コメント**</span><span class="sxs-lookup"><span data-stu-id="2ab3e-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2ab3e-148">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="2ab3e-148">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="2ab3e-149">CMyMAPIFormViewer::CallDoVerb</span><span class="sxs-lookup"><span data-stu-id="2ab3e-149">CMyMAPIFormViewer::CallDoVerb</span></span>  <br/> |<span data-ttu-id="2ab3e-150">MFCMAPI は **IMAPIForm::D oVerb** メソッドを使用して、フォーム上で動詞を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2ab3e-150">MFCMAPI uses the **IMAPIForm::DoVerb** method to invoke a verb on a form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ab3e-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ab3e-151">See also</span></span>



[<span data-ttu-id="2ab3e-152">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="2ab3e-152">IMAPIForm::SetViewContext</span></span>](imapiform-setviewcontext.md)
  
[<span data-ttu-id="2ab3e-153">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="2ab3e-153">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="2ab3e-154">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ab3e-154">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


<span data-ttu-id="2ab3e-155">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2ab3e-155">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="2ab3e-156">フォーム動詞</span><span class="sxs-lookup"><span data-stu-id="2ab3e-156">Form Verbs</span></span>](form-verbs.md)

