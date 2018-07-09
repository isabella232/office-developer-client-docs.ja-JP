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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0451d8635848705ef912b9a575d6390898251f4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800597"
---
# <a name="imapimessagesitemovemessage"></a><span data-ttu-id="723dc-103">IMAPIMessageSite::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="723dc-103">IMAPIMessageSite::MoveMessage</span></span>

  
  
<span data-ttu-id="723dc-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="723dc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="723dc-105">現在のメッセージをフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="723dc-105">Moves the current message to a folder.</span></span>
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="723dc-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="723dc-106">Parameters</span></span>

 <span data-ttu-id="723dc-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="723dc-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="723dc-108">[in]メッセージの移動先フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="723dc-108">[in] A pointer to the folder where the message is to be moved.</span></span>
    
 <span data-ttu-id="723dc-109">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="723dc-109">_pViewContext_</span></span>
  
> <span data-ttu-id="723dc-110">[in]ビュー コンテキスト オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="723dc-110">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="723dc-111">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="723dc-111">_prcPosRect_</span></span>
  
> <span data-ttu-id="723dc-112">[in]現在のフォームのウィンドウのサイズと位置を含む[RECT](http://msdn.microsoft.com/ja-jp/library/dd162897%28VS.85%29.aspx)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="723dc-112">[in] A pointer to a [RECT](http://msdn.microsoft.com/ja-jp/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="723dc-113">次に表示されるフォームは、このウィンドウの四角形にも使用します。</span><span class="sxs-lookup"><span data-stu-id="723dc-113">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="723dc-114">�߂�l</span><span class="sxs-lookup"><span data-stu-id="723dc-114">Return value</span></span>

<span data-ttu-id="723dc-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="723dc-115">S_OK</span></span> 
  
> <span data-ttu-id="723dc-116">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="723dc-116">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="723dc-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="723dc-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="723dc-118">このメッセージのサイトでは、操作はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="723dc-118">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="723dc-119">備考</span><span class="sxs-lookup"><span data-stu-id="723dc-119">Remarks</span></span>

<span data-ttu-id="723dc-120">フォーム オブジェクトは、現在のメッセージを新しいフォルダーに移動するのには**IMAPIMessageSite::MoveMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="723dc-120">Form objects call the **IMAPIMessageSite::MoveMessage** method to move the current message to a new folder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="723dc-121">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="723dc-121">Notes to implementers</span></span>

<span data-ttu-id="723dc-122">**MoveMessage**フォーム ビューアーの実装では、 [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)メソッドは、実際にメッセージを新しいフォルダーに移動する前に、VCDIR_MOVE フラグを渡すことを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="723dc-122">A form viewer's implementation of **MoveMessage** must call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method, passing the VCDIR_MOVE flag, before actually moving the message to a new folder.</span></span> <span data-ttu-id="723dc-123">フォームのウィンドウで使用されている**RECT**構造体を取得するには、Windows[ハンドル](http://msdn.microsoft.com/ja-jp/library/ms633519)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="723dc-123">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](http://msdn.microsoft.com/ja-jp/library/ms633519) function.</span></span> 
  
<span data-ttu-id="723dc-124">フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="723dc-124">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="723dc-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="723dc-125">Notes to callers</span></span>

<span data-ttu-id="723dc-126">**MoveMessage**の戻り値は、次のフォームは現在のメッセージを確認し、存在しない場合はそれ自体を終了して必要があります。</span><span class="sxs-lookup"><span data-stu-id="723dc-126">Following the return of **MoveMessage**, forms must check for a current message and then dismiss themselves if none exists.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="723dc-127">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="723dc-127">MFCMAPI reference</span></span>

<span data-ttu-id="723dc-128">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="723dc-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="723dc-129">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="723dc-129">**File**</span></span>|<span data-ttu-id="723dc-130">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="723dc-130">**Function**</span></span>|<span data-ttu-id="723dc-131">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="723dc-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="723dc-132">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="723dc-132">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="723dc-133">CMyMAPIFormViewer::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="723dc-133">CMyMAPIFormViewer::MoveMessage</span></span>  <br/> |<span data-ttu-id="723dc-134">実装されていません。</span><span class="sxs-lookup"><span data-stu-id="723dc-134">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="723dc-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="723dc-135">See also</span></span>



[<span data-ttu-id="723dc-136">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="723dc-136">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="723dc-137">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="723dc-137">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="723dc-138">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="723dc-138">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="723dc-139">MAPI フォームのインタ フェース</span><span class="sxs-lookup"><span data-stu-id="723dc-139">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

