---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c1ba49ba1b4deacb684da1411d86ebd4dd19e63f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800513"
---
# <a name="imapiformsetviewcontext"></a><span data-ttu-id="f2d8f-103">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="f2d8f-103">IMAPIForm::SetViewContext</span></span>

  
  
<span data-ttu-id="f2d8f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f2d8f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f2d8f-105">フォームのビュー コンテキストを確立します。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-105">Establishes a view context for the form.</span></span> 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="f2d8f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f2d8f-106">Parameters</span></span>

 <span data-ttu-id="f2d8f-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="f2d8f-107">_pViewContext_</span></span>
  
> <span data-ttu-id="f2d8f-108">[in]フォームの新しいビューのコンテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-108">[in] A pointer to the new view context for the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f2d8f-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f2d8f-109">Return value</span></span>

<span data-ttu-id="f2d8f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2d8f-110">S_OK</span></span> 
  
> <span data-ttu-id="f2d8f-111">ビュー コンテキストが正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-111">The view context was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2d8f-112">備考</span><span class="sxs-lookup"><span data-stu-id="f2d8f-112">Remarks</span></span>

<span data-ttu-id="f2d8f-113">フォーム ビューアーは、現在として、特定のフォーム ビューのコンテキストを確立するために**IMAPIForm::SetViewContext**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-113">Form viewers call the **IMAPIForm::SetViewContext** method to establish a particular form view context as current.</span></span> <span data-ttu-id="f2d8f-114">フォームでは、同時にのみ 1 つのビュー コンテキストを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-114">A form can have only one view context at a time.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f2d8f-115">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="f2d8f-115">Notes to implementers</span></span>

<span data-ttu-id="f2d8f-116">フォームのほとんどのサーバーは、次のアルゴリズムを使用して、 **SetViewContext**を実装します。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-116">Most form servers implement **SetViewContext** by using the following algorithm:</span></span> 
  
- <span data-ttu-id="f2d8f-117">_Pmnvs_のパラメーターに**null**に[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出すことによって、フォームの登録を取り消すし、ビュー コンテキスト[リ ス](http://msdn.microsoft.com/ja-jp/library/ms682317%28v=VS.85%29.aspx)を呼び出して、フォームのビューのコンテキストが既に存在する場合参照カウントをデクリメントするメソッドです。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-117">If a view context already exists for the form, cancel the form's registration by calling the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method with **null** in the  _pmnvs_ parameter, and then call the view context's [IUnknown::Release](http://msdn.microsoft.com/ja-jp/library/ms682317%28v=VS.85%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="f2d8f-118">新しいビューのコンテキストが**null**でない場合、新しいビューを設定するのには、 _pViewContext_パラメーターを使用して、 **IMAPIViewContext::SetAdviseSink**の呼び出しは、シンクを案内します。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-118">If the new view context is not **null**, call **IMAPIViewContext::SetAdviseSink** by using the  _pViewContext_ parameter to set up a new view advise sink.</span></span> 
    
- <span data-ttu-id="f2d8f-119">新しいビューのコンテキストが**null**でない場合は、のどの状態フラグが設定されている確認するのには[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-119">If the new view context is not **null**, call the [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method to determine which status flags have been set.</span></span> 
    
- <span data-ttu-id="f2d8f-120">新しいビューのコンテキストが**null**でない場合は、格納し、その参照カウントをインクリメントするには、その[IUnknown::AddRef](http://msdn.microsoft.com/ja-jp/library/ms691379%28VS.85%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-120">If the new view context is not **null**, store it and call its [IUnknown::AddRef](http://msdn.microsoft.com/ja-jp/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> 
    
- <span data-ttu-id="f2d8f-121">ビューのコンテキストに依存するすべてのユーザー インターフェイス要素を更新します。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-121">Update any user interface elements that depend on the view context.</span></span> 
    
<span data-ttu-id="f2d8f-122">**IMAPIViewContext::GetViewStatus**から返されるステータスのフラグに応じて、 **SetViewContext**は他のアクションも実行できます。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-122">Depending on the status flags returned from **IMAPIViewContext::GetViewStatus**, **SetViewContext** can also perform other actions.</span></span> <span data-ttu-id="f2d8f-123">たとえば、VCSTATUS_NEXT および VCSTATUS_PREV のフラグが返される場合、 **SetViewContext**は新しいビュー コンテキストの**次**または**前**のボタンを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-123">For example, if the VCSTATUS_NEXT and VCSTATUS_PREV flags are returned, **SetViewContext** can enable the **Next** and **Previous** buttons for the new view context.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f2d8f-124">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="f2d8f-124">MFCMAPI reference</span></span>

<span data-ttu-id="f2d8f-125">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="f2d8f-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f2d8f-126">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="f2d8f-126">**File**</span></span>|<span data-ttu-id="f2d8f-127">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="f2d8f-127">**Function**</span></span>|<span data-ttu-id="f2d8f-128">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="f2d8f-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f2d8f-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="f2d8f-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f2d8f-130">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="f2d8f-130">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="f2d8f-131">MFCMAPI では、 **IMAPIForm::SetViewContext**メソッドを使用して、フォームが表示される前に、フォームの MFCMAPI のビュー コンテキストを設定します。</span><span class="sxs-lookup"><span data-stu-id="f2d8f-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2d8f-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2d8f-132">See also</span></span>



[<span data-ttu-id="f2d8f-133">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="f2d8f-133">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="f2d8f-134">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f2d8f-134">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="f2d8f-135">IMAPIForm: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f2d8f-135">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


<span data-ttu-id="f2d8f-136">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="f2d8f-136">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

