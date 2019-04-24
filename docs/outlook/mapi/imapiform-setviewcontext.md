---
title: imapiformsetviewcontext
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350947"
---
# <a name="imapiformsetviewcontext"></a><span data-ttu-id="2711f-103">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="2711f-103">IMAPIForm::SetViewContext</span></span>

  
  
<span data-ttu-id="2711f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2711f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2711f-105">フォームのビューコンテキストを確立します。</span><span class="sxs-lookup"><span data-stu-id="2711f-105">Establishes a view context for the form.</span></span> 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="2711f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2711f-106">Parameters</span></span>

 <span data-ttu-id="2711f-107">_pviewcontext_</span><span class="sxs-lookup"><span data-stu-id="2711f-107">_pViewContext_</span></span>
  
> <span data-ttu-id="2711f-108">順番フォームの新しいビューコンテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2711f-108">[in] A pointer to the new view context for the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2711f-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="2711f-109">Return value</span></span>

<span data-ttu-id="2711f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2711f-110">S_OK</span></span> 
  
> <span data-ttu-id="2711f-111">ビューコンテキストが正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="2711f-111">The view context was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2711f-112">解説</span><span class="sxs-lookup"><span data-stu-id="2711f-112">Remarks</span></span>

<span data-ttu-id="2711f-113">フォームビューアーは、 **imapiform:: setviewcontext**メソッドを呼び出して、特定のフォームビューコンテキストを current として設定します。</span><span class="sxs-lookup"><span data-stu-id="2711f-113">Form viewers call the **IMAPIForm::SetViewContext** method to establish a particular form view context as current.</span></span> <span data-ttu-id="2711f-114">フォームは、一度に1つのビューコンテキストのみを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="2711f-114">A form can have only one view context at a time.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2711f-115">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="2711f-115">Notes to implementers</span></span>

<span data-ttu-id="2711f-116">ほとんどのフォームサーバーは、次のアルゴリズムを使用して**setviewcontext**を実装します。</span><span class="sxs-lookup"><span data-stu-id="2711f-116">Most form servers implement **SetViewContext** by using the following algorithm:</span></span> 
  
- <span data-ttu-id="2711f-117">フォームのビューコンテキストが既に存在する場合は、 _pmnvs_パラメーターに**null**を指定して[imapiviewcontext:: SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出して、フォームの登録をキャンセルし、ビューコンテキストの[IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)を呼び出します。メソッドは、その参照カウントをデクリメントします。</span><span class="sxs-lookup"><span data-stu-id="2711f-117">If a view context already exists for the form, cancel the form's registration by calling the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method with **null** in the  _pmnvs_ parameter, and then call the view context's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="2711f-118">新しいビューコンテキストが**null**でない場合は、 _pviewcontext_パラメーターを使用して**imapiviewcontext:: SetAdviseSink**を呼び出し、新しいビューアドバイズシンクを設定します。</span><span class="sxs-lookup"><span data-stu-id="2711f-118">If the new view context is not **null**, call **IMAPIViewContext::SetAdviseSink** by using the  _pViewContext_ parameter to set up a new view advise sink.</span></span> 
    
- <span data-ttu-id="2711f-119">新しいビューコンテキストが**null**でない場合は、 [imapiviewcontext:: getviewstatus](imapiviewcontext-getviewstatus.md)メソッドを呼び出して、どの状態フラグが設定されているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2711f-119">If the new view context is not **null**, call the [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method to determine which status flags have been set.</span></span> 
    
- <span data-ttu-id="2711f-120">新しいビューコンテキストが**null**でない場合は、それを格納して、その参照カウントをインクリメントするように[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2711f-120">If the new view context is not **null**, store it and call its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> 
    
- <span data-ttu-id="2711f-121">ビューコンテキストに依存するユーザーインターフェイス要素を更新します。</span><span class="sxs-lookup"><span data-stu-id="2711f-121">Update any user interface elements that depend on the view context.</span></span> 
    
<span data-ttu-id="2711f-122">**imapiviewcontext:: getviewstatus**から返されるステータスフラグによっては、 **setviewcontext**で他のアクションを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="2711f-122">Depending on the status flags returned from **IMAPIViewContext::GetViewStatus**, **SetViewContext** can also perform other actions.</span></span> <span data-ttu-id="2711f-123">たとえば、VCSTATUS_NEXT と VCSTATUS_PREV のフラグが返された場合、 **setviewcontext**は新しいビューコンテキストに対して**次**のボタンと**前**のボタンを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2711f-123">For example, if the VCSTATUS_NEXT and VCSTATUS_PREV flags are returned, **SetViewContext** can enable the **Next** and **Previous** buttons for the new view context.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2711f-124">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="2711f-124">MFCMAPI reference</span></span>

<span data-ttu-id="2711f-125">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2711f-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2711f-126">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="2711f-126">**File**</span></span>|<span data-ttu-id="2711f-127">**関数**</span><span class="sxs-lookup"><span data-stu-id="2711f-127">**Function**</span></span>|<span data-ttu-id="2711f-128">**コメント**</span><span class="sxs-lookup"><span data-stu-id="2711f-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2711f-129">MAPIFormFunctions</span><span class="sxs-lookup"><span data-stu-id="2711f-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2711f-130">createanddisplaynewmailinfolder</span><span class="sxs-lookup"><span data-stu-id="2711f-130">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="2711f-131">mfcmapi は、 **imapiform:: setviewcontext**メソッドを使用して、フォームが表示される前にフォーム上に mfcmapi のビューコンテキストを設定します。</span><span class="sxs-lookup"><span data-stu-id="2711f-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2711f-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="2711f-132">See also</span></span>



[<span data-ttu-id="2711f-133">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="2711f-133">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="2711f-134">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="2711f-134">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="2711f-135">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2711f-135">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


<span data-ttu-id="2711f-136">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2711f-136">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

