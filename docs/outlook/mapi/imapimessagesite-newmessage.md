---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438772"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="bb54c-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="bb54c-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="bb54c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb54c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb54c-105">新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="bb54c-105">Creates a new message.</span></span>
  
```cpp
HRESULT NewMessage(
  ULONG fComposeInFolder,
  LPMAPIFOLDER pFolderFocus,
  LPPERSISTMESSAGE pPersistMessage,
  LPMESSAGE FAR * ppMessage,
  LPMAPIMESSAGESITE FAR * ppMessageSite,
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="bb54c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bb54c-106">Parameters</span></span>

 <span data-ttu-id="bb54c-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="bb54c-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="bb54c-108">[in]メッセージを構成するフォルダーを示します。</span><span class="sxs-lookup"><span data-stu-id="bb54c-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="bb54c-109">変数が FALSE の場合  _、pFolderFocus_ パラメーターは無視され、フォーム ビューアーは任意のフォルダーでメッセージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="bb54c-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="bb54c-110">変数が TRUE で  _、pFolderFocus_ パラメーターに NULL が渡された場合、メッセージは現在のフォルダーで構成されます。</span><span class="sxs-lookup"><span data-stu-id="bb54c-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="bb54c-111">変数が TRUE で、null 以外の値が  _pFolderFocus_ で渡される場合、メッセージは  _pFolderFocus_ が指すフォルダーで構成されます。</span><span class="sxs-lookup"><span data-stu-id="bb54c-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="bb54c-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="bb54c-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="bb54c-113">[in]新しいメッセージが作成されるフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bb54c-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="bb54c-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="bb54c-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="bb54c-115">[in]新しいフォームのフォーム オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bb54c-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="bb54c-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="bb54c-116">_ppMessage_</span></span>
  
> <span data-ttu-id="bb54c-117">[out]新しいメッセージへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="bb54c-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="bb54c-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="bb54c-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="bb54c-119">[out]新しいメッセージのメッセージ サイト オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bb54c-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="bb54c-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="bb54c-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="bb54c-121">[out]新しいメッセージで新しいフォームに渡すのに適したビュー コンテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bb54c-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="bb54c-122">フォームが独自のビュー コンテキストを実装している場合は  _、ppViewContext_ パラメーターで NULL を渡す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bb54c-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bb54c-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="bb54c-123">Return value</span></span>

<span data-ttu-id="bb54c-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb54c-124">S_OK</span></span> 
  
> <span data-ttu-id="bb54c-125">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="bb54c-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb54c-126">注釈</span><span class="sxs-lookup"><span data-stu-id="bb54c-126">Remarks</span></span>

<span data-ttu-id="bb54c-127">フォーム オブジェクトは **IMAPIMessageSite::NewMessage** メソッドを呼び出して新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="bb54c-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="bb54c-128">フォームは **NewMessage を使用** して、ビューから新しいメッセージと関連付けられたメッセージ サイトを取得します。</span><span class="sxs-lookup"><span data-stu-id="bb54c-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="bb54c-129">その後、新しいメッセージを変更できます。</span><span class="sxs-lookup"><span data-stu-id="bb54c-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="bb54c-130">_ppViewContext_ パラメーターに NULL 以外の値を渡して、関連付けられたビュー コンテキストを取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="bb54c-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="bb54c-131">このビュー コンテキストを直接使用するか、集計して新しいメッセージに渡します。</span><span class="sxs-lookup"><span data-stu-id="bb54c-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="bb54c-132">完全な実装が必要な場合は  _、ppViewContext で NULL を渡します_。</span><span class="sxs-lookup"><span data-stu-id="bb54c-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="bb54c-133">フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="bb54c-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bb54c-134">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="bb54c-134">MFCMAPI reference</span></span>

<span data-ttu-id="bb54c-135">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb54c-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bb54c-136">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="bb54c-136">**File**</span></span>|<span data-ttu-id="bb54c-137">**関数**</span><span class="sxs-lookup"><span data-stu-id="bb54c-137">**Function**</span></span>|<span data-ttu-id="bb54c-138">**コメント**</span><span class="sxs-lookup"><span data-stu-id="bb54c-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb54c-139">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="bb54c-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="bb54c-140">CMyMAPIFormViewer::NewMessage</span><span class="sxs-lookup"><span data-stu-id="bb54c-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="bb54c-141">MFCMAPI は **IMAPIMessageSite::NewMessage** メソッドを使用して、新しいメッセージを作成し、新しいフォーム ビューアーをインスタンス化し **、SetPersist** を呼び出してフォーム ビューアーにメッセージを設定します。</span><span class="sxs-lookup"><span data-stu-id="bb54c-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="bb54c-142">最後に、フォーム ビューアーをメッセージ サイトとして返します。</span><span class="sxs-lookup"><span data-stu-id="bb54c-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb54c-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb54c-143">See also</span></span>



[<span data-ttu-id="bb54c-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb54c-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="bb54c-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb54c-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="bb54c-146">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="bb54c-146">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="bb54c-147">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="bb54c-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

