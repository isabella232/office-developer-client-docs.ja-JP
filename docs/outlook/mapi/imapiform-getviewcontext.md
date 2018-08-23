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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9f09f29d67bff6588c826b92d93aead491510cef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574819"
---
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="a4f29-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="a4f29-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="a4f29-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4f29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4f29-105">フォームの現在のビュー コンテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="a4f29-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="a4f29-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a4f29-106">Parameters</span></span>

 <span data-ttu-id="a4f29-107">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="a4f29-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="a4f29-108">[out]フォームのビューのコンテキストへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a4f29-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4f29-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a4f29-109">Return value</span></span>

<span data-ttu-id="a4f29-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4f29-110">S_OK</span></span> 
  
> <span data-ttu-id="a4f29-111">フォームの現在のビューのコンテキストが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="a4f29-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="a4f29-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="a4f29-112">S_FALSE</span></span> 
  
> <span data-ttu-id="a4f29-113">フォームのビューのコンテキストがありません。</span><span class="sxs-lookup"><span data-stu-id="a4f29-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4f29-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a4f29-114">Remarks</span></span>

<span data-ttu-id="a4f29-115">フォームの閲覧者は、 [IMAPIForm::SetViewContext](imapiform-setviewcontext.md)以前の呼び出しで確立されたビュー コンテキストへのポインターを取得するのには**GetViewContext**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a4f29-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="a4f29-116">以前の呼び出しが作成されなかった場合に**SetViewContext**、 **GetViewContext**は、 _ppViewContext_を NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="a4f29-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a4f29-117">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="a4f29-117">Notes to implementers</span></span>

<span data-ttu-id="a4f29-118">フォームのビュー コンテキスト ポインターを_ppViewContext_パラメーターで呼び出し元のフォーム ビューアーから渡されたポインターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a4f29-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="a4f29-119">フォームがビューのコンテキストを持たない場合は、 _ppViewContext_を NULL に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a4f29-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a4f29-120">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="a4f29-120">MFCMAPI reference</span></span>

<span data-ttu-id="a4f29-121">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="a4f29-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a4f29-122">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="a4f29-122">**File**</span></span>|<span data-ttu-id="a4f29-123">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="a4f29-123">**Function**</span></span>|<span data-ttu-id="a4f29-124">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="a4f29-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a4f29-125">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a4f29-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a4f29-126">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="a4f29-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="a4f29-127">MFCMAPI では、 **IMAPIForm::GetViewContext**メソッドを使用して、フォーム ビューのコンテキストを持つかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a4f29-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4f29-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="a4f29-128">See also</span></span>



[<span data-ttu-id="a4f29-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4f29-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="a4f29-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4f29-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


<span data-ttu-id="a4f29-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="a4f29-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

