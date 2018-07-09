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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9ea44c9ba75390f06ff12ddeed0c7b652538e07d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800538"
---
# <a name="imapiformdoverb"></a><span data-ttu-id="9871f-103">IMAPIForm::DoVerb</span><span class="sxs-lookup"><span data-stu-id="9871f-103">IMAPIForm::DoVerb</span></span>

  
  
<span data-ttu-id="9871f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9871f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9871f-105">フォームは、タスクをどのような実行要求は、特定の動作に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="9871f-105">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="9871f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9871f-106">Parameters</span></span>

 <span data-ttu-id="9871f-107">_iVerb_</span><span class="sxs-lookup"><span data-stu-id="9871f-107">_iVerb_</span></span>
  
> <span data-ttu-id="9871f-108">[in]フォームの動作のいずれかに関連付けられている番号です。</span><span class="sxs-lookup"><span data-stu-id="9871f-108">[in] The number associated with one of the form's verbs.</span></span>
    
 <span data-ttu-id="9871f-109">_lpViewContext_</span><span class="sxs-lookup"><span data-stu-id="9871f-109">_lpViewContext_</span></span>
  
> <span data-ttu-id="9871f-110">[in]ビュー コンテキスト オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9871f-110">[in] A pointer to a view context object.</span></span> <span data-ttu-id="9871f-111">_LpViewContext_パラメーターを**null**にすることができます。</span><span class="sxs-lookup"><span data-stu-id="9871f-111">The  _lpViewContext_ parameter can be **null**.</span></span>
    
 <span data-ttu-id="9871f-112">_hwndParent_</span><span class="sxs-lookup"><span data-stu-id="9871f-112">_hwndParent_</span></span>
  
> <span data-ttu-id="9871f-113">[in]ダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドルを表示します。</span><span class="sxs-lookup"><span data-stu-id="9871f-113">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="9871f-114">ダイアログ ボックスまたはウィンドウがモーダルではない場合、 _hwndParent_パラメーターを**null**にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9871f-114">The  _hwndParent_ parameter should be **null** if the dialog box or window is not modal.</span></span> 
    
 <span data-ttu-id="9871f-115">_lprcPosRect_</span><span class="sxs-lookup"><span data-stu-id="9871f-115">_lprcPosRect_</span></span>
  
> <span data-ttu-id="9871f-116">[in]Win32 へのポインターのサイズと、フォームのウィンドウの位置を含む[RECT](http://msdn.microsoft.com/ja-jp/library/dd162897%28VS.85%29.aspx)構造体。</span><span class="sxs-lookup"><span data-stu-id="9871f-116">[in] A pointer to a Win32 [RECT](http://msdn.microsoft.com/ja-jp/library/dd162897%28VS.85%29.aspx) structure that contains the size and position of the form's window.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9871f-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="9871f-117">Return value</span></span>

<span data-ttu-id="9871f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9871f-118">S_OK</span></span> 
  
> <span data-ttu-id="9871f-119">動詞は正常に呼び出されました。</span><span class="sxs-lookup"><span data-stu-id="9871f-119">The verb was successfully invoked.</span></span>
    
<span data-ttu-id="9871f-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span><span class="sxs-lookup"><span data-stu-id="9871f-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span></span> 
  
> <span data-ttu-id="9871f-121">_IVerb_パラメーターによって表される動詞が有効ですが、フォームがそれに関連付けられている操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="9871f-121">The verb represented by the  _iVerb_ parameter is valid, but the form cannot perform the operations currently associated with it.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9871f-122">備考</span><span class="sxs-lookup"><span data-stu-id="9871f-122">Remarks</span></span>

<span data-ttu-id="9871f-123">フォームの閲覧者は、フォームがフォームをサポートしている各動詞に関連付けることのタスクを実行することを要求する**IMAPIForm::DoVerb**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9871f-123">Form viewers call the **IMAPIForm::DoVerb** method to request that the form perform the tasks that it associates with each verb that the form supports.</span></span> 
  
<span data-ttu-id="9871f-124">_IVerb_パラメーターで**DoVerb**に渡される数値はそれぞれ、サポートされている識別されます。</span><span class="sxs-lookup"><span data-stu-id="9871f-124">Each of the supported verbs is identified by a numeric value, passed to **DoVerb** in the  _iVerb_ parameter.</span></span> <span data-ttu-id="9871f-125">**DoVerb**の典型的な実装には、フォームの_iVerb_パラメーターに有効な値をテストする**switch**ステートメントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9871f-125">Typical implementations of **DoVerb** contain a **switch** statement that tests the values that are valid for the  _iVerb_ parameter for the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9871f-126">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="9871f-126">Notes to implementers</span></span>

<span data-ttu-id="9871f-127">フォーム ビューアーは、 _lpViewContext_パラメーターで、ビューのコンテキストを指定する場合は、 [IMAPIForm::SetViewContext](imapiform-setviewcontext.md)メソッドの以前の呼び出しに渡されるビューのコンテキストではなく、 **DoVerb**の実装に使用します。</span><span class="sxs-lookup"><span data-stu-id="9871f-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span></span> <span data-ttu-id="9871f-128">変更を行いどのような内部データ構造体に必要なビューのコンテキストを保存できません。</span><span class="sxs-lookup"><span data-stu-id="9871f-128">Make whatever changes are necessary to your internal data structures and do not save the view context.</span></span> 
  
<span data-ttu-id="9871f-129">**DoVerb**実装では、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9871f-129">Perform the following tasks in your **DoVerb** implementation:</span></span> 
  
- <span data-ttu-id="9871f-130">_IVerb_パラメーターに関連付けられている特定の動詞のために必要な任意のコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="9871f-130">Execute whatever code is necessary for the particular verb that is associated with the  _iVerb_ parameter.</span></span> 
    
- <span data-ttu-id="9871f-131">必要に応じて、元のビュー コンテキストを復元します。</span><span class="sxs-lookup"><span data-stu-id="9871f-131">If necessary, restore the original view context.</span></span>
    
- <span data-ttu-id="9871f-132">不明な動詞の数が渡された場合は、MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="9871f-132">If an unknown verb number was passed in, return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="9871f-133">それ以外の場合、どのような動詞の実行の成否に基づいて結果を返します。</span><span class="sxs-lookup"><span data-stu-id="9871f-133">Otherwise, return a result based on the success or failure of whatever verb was executed.</span></span>
    
- <span data-ttu-id="9871f-134">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9871f-134">Close the form.</span></span> <span data-ttu-id="9871f-135">**DoVerb**呼び出しが完了した後、フォームを閉じる必要が常にします。</span><span class="sxs-lookup"><span data-stu-id="9871f-135">It is always your responsibility to close the form after a **DoVerb** call completes.</span></span> 
    
<span data-ttu-id="9871f-136">印刷などのいくつかの動詞は、**これら**に対してはモーダルである必要があります-つまり、 **DoVerb**呼び出しから戻る前にした操作を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9871f-136">Some verbs, such as Print, should be modal with respect to the **DoVerb** call — that is, the indicated operation must be finished before the **DoVerb** call returns.</span></span> 
  
<span data-ttu-id="9871f-137">フォームのウィンドウで使用されている**RECT**構造体を取得するには、[受け取り](http://msdn.microsoft.com/ja-jp/library/ms633519)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9871f-137">To obtain the **RECT** structure used by a form's window, call the [GetWindowRect](http://msdn.microsoft.com/ja-jp/library/ms633519) function.</span></span> 
  
<span data-ttu-id="9871f-138">通常は、 **DoVerb**が完了するまで、そのことができますすぐに破棄する呼び出しの戻り値にするため、 _hwndParent_パラメーターのハンドルを保存しません。</span><span class="sxs-lookup"><span data-stu-id="9871f-138">Do not save the handle in the  _hwndParent_ parameter because, although it usually remains valid until the completion of **DoVerb**, it can be destroyed immediately upon the call's return.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="9871f-139">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="9871f-139">Notes to callers</span></span>

<span data-ttu-id="9871f-140">_LpViewContext_ ] をポイントして、 [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)メソッドから、VCSTATUS_MODAL フラグを返すビュー コンテキストの実装のモーダル動詞として機能する非モーダル動詞を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9871f-140">You can make non-modal verbs act as modal verbs by pointing  _lpViewContext_ to a view context implementation that returns the VCSTATUS_MODAL flag from its [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
  
<span data-ttu-id="9871f-141">MAPI での動詞の詳細については、[動詞のフォーム](form-verbs.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9871f-141">For more information about verbs in MAPI, see [Form Verbs](form-verbs.md).</span></span> <span data-ttu-id="9871f-142">OLE 動詞を処理する方法の詳細については、 [OLE アプリケーションとデータの転送](http://msdn.microsoft.com/ja-jp/library/ms693425%28VS.85%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9871f-142">For more information about how verbs are handled in OLE, see [OLE and Data Transfer](http://msdn.microsoft.com/ja-jp/library/ms693425%28VS.85%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9871f-143">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="9871f-143">MFCMAPI reference</span></span>

<span data-ttu-id="9871f-144">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="9871f-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9871f-145">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="9871f-145">**File**</span></span>|<span data-ttu-id="9871f-146">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="9871f-146">**Function**</span></span>|<span data-ttu-id="9871f-147">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="9871f-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9871f-148">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="9871f-148">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="9871f-149">CMyMAPIFormViewer::CallDoVerb</span><span class="sxs-lookup"><span data-stu-id="9871f-149">CMyMAPIFormViewer::CallDoVerb</span></span>  <br/> |<span data-ttu-id="9871f-150">MFCMAPI では、 **IMAPIForm::DoVerb**メソッドを使用して、フォーム上の動詞を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9871f-150">MFCMAPI uses the **IMAPIForm::DoVerb** method to invoke a verb on a form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9871f-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="9871f-151">See also</span></span>



[<span data-ttu-id="9871f-152">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="9871f-152">IMAPIForm::SetViewContext</span></span>](imapiform-setviewcontext.md)
  
[<span data-ttu-id="9871f-153">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="9871f-153">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="9871f-154">IMAPIForm: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9871f-154">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


<span data-ttu-id="9871f-155">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="9871f-155">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="9871f-156">フォームの動詞</span><span class="sxs-lookup"><span data-stu-id="9871f-156">Form Verbs</span></span>](form-verbs.md)

