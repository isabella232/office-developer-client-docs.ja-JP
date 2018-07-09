---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: da6de94342c8d8bbd378a3cde2fb065c97632291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800582"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="5858d-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="5858d-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="5858d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5858d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5858d-105">現在のメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="5858d-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="5858d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5858d-106">Parameters</span></span>

 <span data-ttu-id="5858d-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="5858d-107">_pViewContext_</span></span>
  
> <span data-ttu-id="5858d-108">[in]ビュー コンテキスト オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5858d-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="5858d-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="5858d-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="5858d-110">[in]現在のフォームのウィンドウのサイズと位置を含む[RECT](http://msdn.microsoft.com/ja-jp/library/dd162897%28VS.85%29.aspx)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5858d-110">[in] A pointer to a [RECT](http://msdn.microsoft.com/ja-jp/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="5858d-111">次に表示されるフォームは、このウィンドウの四角形にも使用します。</span><span class="sxs-lookup"><span data-stu-id="5858d-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5858d-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5858d-112">Return value</span></span>

<span data-ttu-id="5858d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="5858d-113">S_OK</span></span> 
  
> <span data-ttu-id="5858d-114">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="5858d-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5858d-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5858d-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5858d-116">このメッセージのサイトでは、操作はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5858d-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5858d-117">備考</span><span class="sxs-lookup"><span data-stu-id="5858d-117">Remarks</span></span>

<span data-ttu-id="5858d-118">フォーム オブジェクトは、フォームが現在表示されているメッセージを削除するのには**IMAPIMessageSite::DeleteMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5858d-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5858d-119">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5858d-119">Notes to callers</span></span>

<span data-ttu-id="5858d-120">**DeleteMessage**の戻り値は、次のフォーム オブジェクトが新しいメッセージを確認し、存在しない場合はそれ自体を終了してください。</span><span class="sxs-lookup"><span data-stu-id="5858d-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="5858d-121">**DeleteMessage**の処理でメッセージが削除またはを**削除済みアイテム**フォルダーに移動するかどうかを確認するのにフォーム オブジェクトは、DELETE_IS_MOVE フラグが返されたかどうかを決定する[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="5858d-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5858d-122">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="5858d-122">Notes to implementers</span></span>

<span data-ttu-id="5858d-123">**DeleteMessage**メソッドの実装をフォームのビューアーの移動する場合、次のメッセージのメッセージを削除した後、実装する必要があります[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)メソッドを呼び出すし、実行する前に VCDIR_DELETE フラグを渡す実際の削除します。</span><span class="sxs-lookup"><span data-stu-id="5858d-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="5858d-124">**DeleteMessage**フォーム ビューアーの実装では、(たとえば、 **[削除済みアイテム**フォルダー) に削除されたメッセージを移動した場合実装は、メッセージが変更された場合は、メッセージに変更を保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5858d-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="5858d-125">**DeleteMessage**の一般的な実装では、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="5858d-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="5858d-126">実装では、メッセージを移動では場合、は、 **null** _pMessage_パラメーターとの**場合は true** 、 _fSameAsLoad_パラメーターに渡して、 [IPersistMessage::Save](ipersistmessage-save.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5858d-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="5858d-127">_UlDir_パラメーターに VCDIR_DELETE フラグを渡す、 **IMAPIViewContext::ActivateNext**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5858d-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="5858d-128">**ActivateNext**の呼び出しが失敗したかどうかを返します。</span><span class="sxs-lookup"><span data-stu-id="5858d-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="5858d-129">**ActivateNext**が S_FALSE を返す場合は、 [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5858d-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="5858d-130">削除または、メッセージを移動します。</span><span class="sxs-lookup"><span data-stu-id="5858d-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="5858d-131">フォームのウィンドウで使用されている**RECT**構造体を取得するには、Windows[ハンドル](http://msdn.microsoft.com/ja-jp/library/ms633519)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5858d-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](http://msdn.microsoft.com/ja-jp/library/ms633519) function.</span></span> 
  
<span data-ttu-id="5858d-132">フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5858d-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5858d-133">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="5858d-133">MFCMAPI reference</span></span>

<span data-ttu-id="5858d-134">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="5858d-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5858d-135">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="5858d-135">**File**</span></span>|<span data-ttu-id="5858d-136">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="5858d-136">**Function**</span></span>|<span data-ttu-id="5858d-137">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="5858d-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5858d-138">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="5858d-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="5858d-139">CMyMAPIFormViewer::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="5858d-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="5858d-140">実装されていません。</span><span class="sxs-lookup"><span data-stu-id="5858d-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5858d-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="5858d-141">See also</span></span>



[<span data-ttu-id="5858d-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="5858d-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="5858d-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="5858d-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="5858d-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="5858d-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="5858d-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="5858d-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="5858d-146">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5858d-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="5858d-147">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="5858d-147">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="5858d-148">MAPI フォームのインタ フェース</span><span class="sxs-lookup"><span data-stu-id="5858d-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

