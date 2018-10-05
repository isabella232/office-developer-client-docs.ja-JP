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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 81d99b2bbe6ef7914a4b7d253a3472026872260d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384312"
---
# <a name="imapiformsetviewcontext"></a><span data-ttu-id="786a1-103">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="786a1-103">IMAPIForm::SetViewContext</span></span>

  
  
<span data-ttu-id="786a1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="786a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="786a1-105">フォームのビュー コンテキストを確立します。</span><span class="sxs-lookup"><span data-stu-id="786a1-105">Establishes a view context for the form.</span></span> 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="786a1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="786a1-106">Parameters</span></span>

 <span data-ttu-id="786a1-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="786a1-107">_pViewContext_</span></span>
  
> <span data-ttu-id="786a1-108">[in]フォームの新しいビューのコンテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="786a1-108">[in] A pointer to the new view context for the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="786a1-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="786a1-109">Return value</span></span>

<span data-ttu-id="786a1-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="786a1-110">S_OK</span></span> 
  
> <span data-ttu-id="786a1-111">ビュー コンテキストが正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="786a1-111">The view context was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="786a1-112">備考</span><span class="sxs-lookup"><span data-stu-id="786a1-112">Remarks</span></span>

<span data-ttu-id="786a1-113">フォーム ビューアーは、現在として、特定のフォーム ビューのコンテキストを確立するために**IMAPIForm::SetViewContext**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="786a1-113">Form viewers call the **IMAPIForm::SetViewContext** method to establish a particular form view context as current.</span></span> <span data-ttu-id="786a1-114">フォームでは、同時にのみ 1 つのビュー コンテキストを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="786a1-114">A form can have only one view context at a time.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="786a1-115">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="786a1-115">Notes to implementers</span></span>

<span data-ttu-id="786a1-116">フォームのほとんどのサーバーは、次のアルゴリズムを使用して、 **SetViewContext**を実装します。</span><span class="sxs-lookup"><span data-stu-id="786a1-116">Most form servers implement **SetViewContext** by using the following algorithm:</span></span> 
  
- <span data-ttu-id="786a1-117">_Pmnvs_のパラメーターに**null**に[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出すことによって、フォームの登録を取り消すし、ビュー コンテキスト[リ ス](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)を呼び出して、フォームのビューのコンテキストが既に存在する場合参照カウントをデクリメントするメソッドです。</span><span class="sxs-lookup"><span data-stu-id="786a1-117">If a view context already exists for the form, cancel the form's registration by calling the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method with **null** in the  _pmnvs_ parameter, and then call the view context's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="786a1-118">新しいビューのコンテキストが**null**でない場合、新しいビューを設定するのには、 _pViewContext_パラメーターを使用して、 **IMAPIViewContext::SetAdviseSink**の呼び出しは、シンクを案内します。</span><span class="sxs-lookup"><span data-stu-id="786a1-118">If the new view context is not **null**, call **IMAPIViewContext::SetAdviseSink** by using the  _pViewContext_ parameter to set up a new view advise sink.</span></span> 
    
- <span data-ttu-id="786a1-119">新しいビューのコンテキストが**null**でない場合は、のどの状態フラグが設定されている確認するのには[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="786a1-119">If the new view context is not **null**, call the [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method to determine which status flags have been set.</span></span> 
    
- <span data-ttu-id="786a1-120">新しいビューのコンテキストが**null**でない場合は、格納し、その参照カウントをインクリメントするには、その[IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="786a1-120">If the new view context is not **null**, store it and call its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> 
    
- <span data-ttu-id="786a1-121">ビューのコンテキストに依存するすべてのユーザー インターフェイス要素を更新します。</span><span class="sxs-lookup"><span data-stu-id="786a1-121">Update any user interface elements that depend on the view context.</span></span> 
    
<span data-ttu-id="786a1-122">**IMAPIViewContext::GetViewStatus**から返されるステータスのフラグに応じて、 **SetViewContext**は他のアクションも実行できます。</span><span class="sxs-lookup"><span data-stu-id="786a1-122">Depending on the status flags returned from **IMAPIViewContext::GetViewStatus**, **SetViewContext** can also perform other actions.</span></span> <span data-ttu-id="786a1-123">たとえば、VCSTATUS_NEXT および VCSTATUS_PREV のフラグが返される場合、 **SetViewContext**は新しいビュー コンテキストの**次**または**前**のボタンを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="786a1-123">For example, if the VCSTATUS_NEXT and VCSTATUS_PREV flags are returned, **SetViewContext** can enable the **Next** and **Previous** buttons for the new view context.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="786a1-124">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="786a1-124">MFCMAPI reference</span></span>

<span data-ttu-id="786a1-125">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="786a1-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="786a1-126">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="786a1-126">**File**</span></span>|<span data-ttu-id="786a1-127">**関数**</span><span class="sxs-lookup"><span data-stu-id="786a1-127">**Function**</span></span>|<span data-ttu-id="786a1-128">**コメント**</span><span class="sxs-lookup"><span data-stu-id="786a1-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="786a1-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="786a1-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="786a1-130">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="786a1-130">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="786a1-131">MFCMAPI では、 **IMAPIForm::SetViewContext**メソッドを使用して、フォームが表示される前に、フォームの MFCMAPI のビュー コンテキストを設定します。</span><span class="sxs-lookup"><span data-stu-id="786a1-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="786a1-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="786a1-132">See also</span></span>



[<span data-ttu-id="786a1-133">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="786a1-133">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="786a1-134">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="786a1-134">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="786a1-135">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="786a1-135">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


<span data-ttu-id="786a1-136">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="786a1-136">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

