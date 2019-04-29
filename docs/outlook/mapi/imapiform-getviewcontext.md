---
title: imapiformgetviewcontext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f0b217372f6b4848f83c993846cd08a81c7098e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430904"
---
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="73283-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="73283-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="73283-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73283-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73283-105">フォームの現在のビューコンテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="73283-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="73283-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="73283-106">Parameters</span></span>

 <span data-ttu-id="73283-107">_ppviewcontext_</span><span class="sxs-lookup"><span data-stu-id="73283-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="73283-108">読み上げフォームのビューコンテキストへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="73283-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="73283-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="73283-109">Return value</span></span>

<span data-ttu-id="73283-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="73283-110">S_OK</span></span> 
  
> <span data-ttu-id="73283-111">フォームの現在のビューコンテキストが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="73283-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="73283-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="73283-112">S_FALSE</span></span> 
  
> <span data-ttu-id="73283-113">フォームにビューコンテキストはありません。</span><span class="sxs-lookup"><span data-stu-id="73283-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73283-114">注釈</span><span class="sxs-lookup"><span data-stu-id="73283-114">Remarks</span></span>

<span data-ttu-id="73283-115">フォーム閲覧者は**getviewcontext**を呼び出して、以前の[imapiform:: setviewcontext](imapiform-setviewcontext.md)への呼び出しで設定されたビューコンテキストへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="73283-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="73283-116">**setviewcontext**に対して前回の呼び出しが行われていない場合、 **getviewcontext**は_ppviewcontext_を NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="73283-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="73283-117">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="73283-117">Notes to implementers</span></span>

<span data-ttu-id="73283-118">フォームのビューコンテキストポインターを、 _ppviewcontext_パラメーターの呼び出し元フォームビューアーによって渡されるポインターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="73283-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="73283-119">フォームにビューコンテキストがない場合は、 _ppviewcontext_を NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="73283-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="73283-120">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="73283-120">MFCMAPI reference</span></span>

<span data-ttu-id="73283-121">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73283-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="73283-122">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="73283-122">**File**</span></span>|<span data-ttu-id="73283-123">**関数**</span><span class="sxs-lookup"><span data-stu-id="73283-123">**Function**</span></span>|<span data-ttu-id="73283-124">**コメント**</span><span class="sxs-lookup"><span data-stu-id="73283-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="73283-125">MAPIFormFunctions</span><span class="sxs-lookup"><span data-stu-id="73283-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="73283-126">openmessagenonmodal</span><span class="sxs-lookup"><span data-stu-id="73283-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="73283-127">mfcmapi は、 **imapiform:: getviewcontext**メソッドを使用して、フォームにビューコンテキストがあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="73283-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73283-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="73283-128">See also</span></span>



[<span data-ttu-id="73283-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="73283-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="73283-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="73283-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


<span data-ttu-id="73283-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="73283-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

