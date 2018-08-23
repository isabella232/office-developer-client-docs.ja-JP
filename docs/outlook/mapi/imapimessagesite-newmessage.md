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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7062e0b73d2d70be12fb9cead6813ef9c36fdd43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800601"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="cfd5b-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="cfd5b-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="cfd5b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cfd5b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cfd5b-105">新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-105">Creates a new message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="cfd5b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cfd5b-106">Parameters</span></span>

 <span data-ttu-id="cfd5b-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="cfd5b-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="cfd5b-108">[in]メッセージので構成されるフォルダーを示します。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="cfd5b-109">変数が FALSE の場合は、 _pFolderFocus_パラメーターは無視され、フォーム ビューアーは、任意のフォルダーにメッセージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="cfd5b-110">変数が TRUE の場合、 _pFolderFocus_パラメーターに NULL が渡されるとは、メッセージが現在のフォルダー内で構成されます。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="cfd5b-111">変数が TRUE を NULL 以外の値が_pFolderFocus_に渡された場合は、メッセージが_pFolderFocus_で指定されたフォルダー内で構成されます。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="cfd5b-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="cfd5b-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="cfd5b-113">[in]新しいメッセージを作成する場所のフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="cfd5b-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="cfd5b-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="cfd5b-115">[in]新しいフォームのフォーム オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="cfd5b-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="cfd5b-116">_ppMessage_</span></span>
  
> <span data-ttu-id="cfd5b-117">[out]新しいメッセージへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="cfd5b-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="cfd5b-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="cfd5b-119">[out]新しいメッセージのメッセージのサイト オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="cfd5b-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="cfd5b-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="cfd5b-121">[out]新しいメッセージを新しいフォームに渡すのための適切なビューのコンテキストへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="cfd5b-122">フォームは、独自のビュー コンテキストを実装する場合は、 _ppViewContext_パラメーターに NULL を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cfd5b-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="cfd5b-123">Return value</span></span>

<span data-ttu-id="cfd5b-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="cfd5b-124">S_OK</span></span> 
  
> <span data-ttu-id="cfd5b-125">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="cfd5b-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cfd5b-126">����</span><span class="sxs-lookup"><span data-stu-id="cfd5b-126">Remarks</span></span>

<span data-ttu-id="cfd5b-127">フォーム オブジェクトは、新しいメッセージを作成する**IMAPIMessageSite::NewMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="cfd5b-128">フォームは、そのビューから新しいメッセージが、メッセージが関連付けられているサイトを取得するのに**NewMessage**を使用します。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="cfd5b-129">新しいメッセージに変更できます。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="cfd5b-130">_PpViewContext_パラメーターに NULL 以外の値を渡すことによって、関連付けられているビューのコンテキストを取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="cfd5b-131">このビューのコンテキストを使用して直接、または集約し、新しいメッセージに渡されることができます。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="cfd5b-132">完全な実装が必要な場合は、 _ppViewContext_に NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="cfd5b-133">フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cfd5b-134">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="cfd5b-134">MFCMAPI reference</span></span>

<span data-ttu-id="cfd5b-135">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="cfd5b-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cfd5b-136">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="cfd5b-136">**File**</span></span>|<span data-ttu-id="cfd5b-137">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="cfd5b-137">**Function**</span></span>|<span data-ttu-id="cfd5b-138">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="cfd5b-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cfd5b-139">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="cfd5b-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="cfd5b-140">CMyMAPIFormViewer::NewMessage</span><span class="sxs-lookup"><span data-stu-id="cfd5b-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="cfd5b-141">MFCMAPI では、 **IMAPIMessageSite::NewMessage**メソッドを使用して、新しいメッセージを作成し、新しいフォームのビューアーをインスタンス化し、フォームのビューアーで、メッセージを設定するのには**SetPersist**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="cfd5b-142">最後に、メッセージのサイトとして、フォームのビューアーを返します。</span><span class="sxs-lookup"><span data-stu-id="cfd5b-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cfd5b-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="cfd5b-143">See also</span></span>



[<span data-ttu-id="cfd5b-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cfd5b-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="cfd5b-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cfd5b-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="cfd5b-146">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="cfd5b-146">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="cfd5b-147">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="cfd5b-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

