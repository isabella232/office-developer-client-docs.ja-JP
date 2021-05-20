---
title: IMAPIFormGetViewContext
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
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="2765c-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="2765c-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="2765c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2765c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2765c-105">フォームの現在のビュー コンテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="2765c-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="2765c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2765c-106">Parameters</span></span>

 <span data-ttu-id="2765c-107">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="2765c-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="2765c-108">[out]フォームのビュー コンテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2765c-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2765c-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="2765c-109">Return value</span></span>

<span data-ttu-id="2765c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2765c-110">S_OK</span></span> 
  
> <span data-ttu-id="2765c-111">フォームの現在のビュー コンテキストが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="2765c-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="2765c-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="2765c-112">S_FALSE</span></span> 
  
> <span data-ttu-id="2765c-113">フォームのビュー コンテキストはありません。</span><span class="sxs-lookup"><span data-stu-id="2765c-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2765c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2765c-114">Remarks</span></span>

<span data-ttu-id="2765c-115">フォーム ビューアーは **GetViewContext** を呼び出して [、IMAPIForm::SetViewContext](imapiform-setviewcontext.md)への以前の呼び出しで確立されたビュー コンテキストへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="2765c-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="2765c-116">**SetViewContext** に対して以前に呼び出しが行われた場合 **、GetViewContext は ppViewContext** _を NULL に_ 設定します。</span><span class="sxs-lookup"><span data-stu-id="2765c-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2765c-117">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="2765c-117">Notes to implementers</span></span>

<span data-ttu-id="2765c-118">_ppViewContext_ パラメーターで呼び出し元のフォーム ビューアーによって渡されたポインターに、フォームのビュー コンテキスト ポインターをコピーします。</span><span class="sxs-lookup"><span data-stu-id="2765c-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="2765c-119">フォームにビュー コンテキストがない場合は  _、ppViewContext を NULL に_ 設定します。</span><span class="sxs-lookup"><span data-stu-id="2765c-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2765c-120">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="2765c-120">MFCMAPI reference</span></span>

<span data-ttu-id="2765c-121">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2765c-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2765c-122">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="2765c-122">**File**</span></span>|<span data-ttu-id="2765c-123">**関数**</span><span class="sxs-lookup"><span data-stu-id="2765c-123">**Function**</span></span>|<span data-ttu-id="2765c-124">**コメント**</span><span class="sxs-lookup"><span data-stu-id="2765c-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2765c-125">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="2765c-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2765c-126">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="2765c-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="2765c-127">MFCMAPI は **IMAPIForm::GetViewContext** メソッドを使用して、フォームにビュー コンテキストが含されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2765c-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2765c-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="2765c-128">See also</span></span>



[<span data-ttu-id="2765c-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2765c-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="2765c-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2765c-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


<span data-ttu-id="2765c-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2765c-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

