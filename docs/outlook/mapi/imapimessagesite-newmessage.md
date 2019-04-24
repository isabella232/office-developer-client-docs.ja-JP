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
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321456"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="485b3-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="485b3-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="485b3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="485b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="485b3-105">新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="485b3-105">Creates a new message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="485b3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="485b3-106">Parameters</span></span>

 <span data-ttu-id="485b3-107">_fて seinfolder_</span><span class="sxs-lookup"><span data-stu-id="485b3-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="485b3-108">順番メッセージを構成するフォルダーを示します。</span><span class="sxs-lookup"><span data-stu-id="485b3-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="485b3-109">変数が FALSE の場合、 _pfolderfocus_パラメーターは無視され、フォームビューアーは任意のフォルダーでメッセージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="485b3-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="485b3-110">変数が TRUE で、 _pfolderfocus_パラメーターで NULL が渡された場合、メッセージは現在のフォルダーで構成されます。</span><span class="sxs-lookup"><span data-stu-id="485b3-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="485b3-111">変数が TRUE で、 _pfolderfocus_で NULL 以外の値が渡された場合、メッセージは_pfolderfocus_が指すフォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="485b3-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="485b3-112">_pfolderfocus_</span><span class="sxs-lookup"><span data-stu-id="485b3-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="485b3-113">順番新しいメッセージが作成されるフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="485b3-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="485b3-114">_ppersistmessage_</span><span class="sxs-lookup"><span data-stu-id="485b3-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="485b3-115">順番新しいフォームの form オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="485b3-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="485b3-116">_ppmessage_</span><span class="sxs-lookup"><span data-stu-id="485b3-116">_ppMessage_</span></span>
  
> <span data-ttu-id="485b3-117">読み上げ新しいメッセージへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="485b3-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="485b3-118">_ppメッセージ ite_</span><span class="sxs-lookup"><span data-stu-id="485b3-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="485b3-119">読み上げ新しいメッセージのメッセージサイトオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="485b3-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="485b3-120">_ppviewcontext_</span><span class="sxs-lookup"><span data-stu-id="485b3-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="485b3-121">読み上げ新しいメッセージを使用して新しいフォームに渡すための適切なビューコンテキストへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="485b3-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="485b3-122">フォームが独自のビューコンテキストを実装している場合は、 _ppviewcontext_パラメーターに NULL を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="485b3-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="485b3-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="485b3-123">Return value</span></span>

<span data-ttu-id="485b3-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="485b3-124">S_OK</span></span> 
  
> <span data-ttu-id="485b3-125">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="485b3-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="485b3-126">解説</span><span class="sxs-lookup"><span data-stu-id="485b3-126">Remarks</span></span>

<span data-ttu-id="485b3-127">Form オブジェクトは、 **IMAPIMessageSite:: newmessage**メソッドを呼び出して、新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="485b3-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="485b3-128">このフォームは、新しいメッセージと関連するメッセージサイトをビューから取得するために、 **newmessage**を使用します。</span><span class="sxs-lookup"><span data-stu-id="485b3-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="485b3-129">その後、新しいメッセージを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="485b3-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="485b3-130">_ppviewcontext_パラメーターに NULL 以外の値を渡すことによって、関連付けられているビューコンテキストを取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="485b3-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="485b3-131">このビューコンテキストは直接使用することも、新しいメッセージに集約して渡すこともできます。</span><span class="sxs-lookup"><span data-stu-id="485b3-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="485b3-132">完全な実装が必要な場合は、 _ppviewcontext_に NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="485b3-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="485b3-133">フォームサーバーに関連するインターフェイスの一覧については、「 [MAPI フォームインターフェイス](mapi-form-interfaces.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="485b3-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="485b3-134">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="485b3-134">MFCMAPI reference</span></span>

<span data-ttu-id="485b3-135">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="485b3-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="485b3-136">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="485b3-136">**File**</span></span>|<span data-ttu-id="485b3-137">**関数**</span><span class="sxs-lookup"><span data-stu-id="485b3-137">**Function**</span></span>|<span data-ttu-id="485b3-138">**コメント**</span><span class="sxs-lookup"><span data-stu-id="485b3-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="485b3-139">MyMAPIFormViewer</span><span class="sxs-lookup"><span data-stu-id="485b3-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="485b3-140">cmymapiformviewer:: newmessage</span><span class="sxs-lookup"><span data-stu-id="485b3-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="485b3-141">mfcmapi は、 **IMAPIMessageSite:: newmessage**メソッドを使用して、新しいメッセージを作成し、新しいフォームビューアーをインスタンス化し、呼び出し**setpersist**を呼び出して、フォームビューアーにメッセージを設定します。</span><span class="sxs-lookup"><span data-stu-id="485b3-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="485b3-142">最後に、フォームビューアーをメッセージサイトとして返します。</span><span class="sxs-lookup"><span data-stu-id="485b3-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="485b3-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="485b3-143">See also</span></span>



[<span data-ttu-id="485b3-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="485b3-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="485b3-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="485b3-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="485b3-146">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="485b3-146">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="485b3-147">MAPI フォームインターフェイス</span><span class="sxs-lookup"><span data-stu-id="485b3-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

