---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382373"
---
# <a name="imapimessagesitemovemessage"></a><span data-ttu-id="d67b8-103">IMAPIMessageSite::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="d67b8-103">IMAPIMessageSite::MoveMessage</span></span>

  
  
<span data-ttu-id="d67b8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d67b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d67b8-105">現在のメッセージをフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="d67b8-105">Moves the current message to a folder.</span></span>
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="d67b8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d67b8-106">Parameters</span></span>

 <span data-ttu-id="d67b8-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="d67b8-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="d67b8-108">[in]メッセージの移動先フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d67b8-108">[in] A pointer to the folder where the message is to be moved.</span></span>
    
 <span data-ttu-id="d67b8-109">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="d67b8-109">_pViewContext_</span></span>
  
> <span data-ttu-id="d67b8-110">[in]ビュー コンテキスト オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d67b8-110">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="d67b8-111">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="d67b8-111">_prcPosRect_</span></span>
  
> <span data-ttu-id="d67b8-112">[in]現在のフォームのウィンドウのサイズと位置を含む[RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d67b8-112">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="d67b8-113">次に表示されるフォームは、このウィンドウの四角形にも使用します。</span><span class="sxs-lookup"><span data-stu-id="d67b8-113">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d67b8-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="d67b8-114">Return value</span></span>

<span data-ttu-id="d67b8-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="d67b8-115">S_OK</span></span> 
  
> <span data-ttu-id="d67b8-116">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="d67b8-116">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d67b8-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d67b8-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d67b8-118">このメッセージのサイトでは、操作はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d67b8-118">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d67b8-119">備考</span><span class="sxs-lookup"><span data-stu-id="d67b8-119">Remarks</span></span>

<span data-ttu-id="d67b8-120">フォーム オブジェクトは、現在のメッセージを新しいフォルダーに移動するのには**IMAPIMessageSite::MoveMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d67b8-120">Form objects call the **IMAPIMessageSite::MoveMessage** method to move the current message to a new folder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d67b8-121">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="d67b8-121">Notes to implementers</span></span>

<span data-ttu-id="d67b8-122">**MoveMessage**フォーム ビューアーの実装では、 [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)メソッドは、実際にメッセージを新しいフォルダーに移動する前に、VCDIR_MOVE フラグを渡すことを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d67b8-122">A form viewer's implementation of **MoveMessage** must call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method, passing the VCDIR_MOVE flag, before actually moving the message to a new folder.</span></span> <span data-ttu-id="d67b8-123">フォームのウィンドウで使用されている**RECT**構造体を取得するには、Windows[ハンドル](https://msdn.microsoft.com/library/ms633519)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d67b8-123">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="d67b8-124">フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d67b8-124">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="d67b8-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d67b8-125">Notes to callers</span></span>

<span data-ttu-id="d67b8-126">**MoveMessage**の戻り値は、次のフォームは現在のメッセージを確認し、存在しない場合はそれ自体を終了して必要があります。</span><span class="sxs-lookup"><span data-stu-id="d67b8-126">Following the return of **MoveMessage**, forms must check for a current message and then dismiss themselves if none exists.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d67b8-127">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="d67b8-127">MFCMAPI reference</span></span>

<span data-ttu-id="d67b8-128">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d67b8-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d67b8-129">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="d67b8-129">**File**</span></span>|<span data-ttu-id="d67b8-130">**関数**</span><span class="sxs-lookup"><span data-stu-id="d67b8-130">**Function**</span></span>|<span data-ttu-id="d67b8-131">**コメント**</span><span class="sxs-lookup"><span data-stu-id="d67b8-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d67b8-132">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="d67b8-132">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d67b8-133">CMyMAPIFormViewer::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="d67b8-133">CMyMAPIFormViewer::MoveMessage</span></span>  <br/> |<span data-ttu-id="d67b8-134">実装されていません。</span><span class="sxs-lookup"><span data-stu-id="d67b8-134">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d67b8-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="d67b8-135">See also</span></span>



[<span data-ttu-id="d67b8-136">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="d67b8-136">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="d67b8-137">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d67b8-137">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="d67b8-138">コード サンプルとしての MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d67b8-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d67b8-139">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d67b8-139">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

