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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6ed73cd683f1668900a76f7b8c48494952e9fc14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573349"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="1488b-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="1488b-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="1488b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1488b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1488b-105">現在のメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="1488b-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="1488b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1488b-106">Parameters</span></span>

 <span data-ttu-id="1488b-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="1488b-107">_pViewContext_</span></span>
  
> <span data-ttu-id="1488b-108">[in]ビュー コンテキスト オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1488b-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="1488b-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="1488b-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="1488b-110">[in]現在のフォームのウィンドウのサイズと位置を含む[RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1488b-110">[in] A pointer to a [RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="1488b-111">次に表示されるフォームは、このウィンドウの四角形にも使用します。</span><span class="sxs-lookup"><span data-stu-id="1488b-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1488b-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1488b-112">Return value</span></span>

<span data-ttu-id="1488b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1488b-113">S_OK</span></span> 
  
> <span data-ttu-id="1488b-114">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="1488b-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1488b-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1488b-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="1488b-116">このメッセージのサイトでは、操作はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1488b-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1488b-117">注釈</span><span class="sxs-lookup"><span data-stu-id="1488b-117">Remarks</span></span>

<span data-ttu-id="1488b-118">フォーム オブジェクトは、フォームが現在表示されているメッセージを削除するのには**IMAPIMessageSite::DeleteMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1488b-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1488b-119">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="1488b-119">Notes to callers</span></span>

<span data-ttu-id="1488b-120">**DeleteMessage**の戻り値は、次のフォーム オブジェクトが新しいメッセージを確認し、存在しない場合はそれ自体を終了してください。</span><span class="sxs-lookup"><span data-stu-id="1488b-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="1488b-121">**DeleteMessage**の処理でメッセージが削除またはを**削除済みアイテム**フォルダーに移動するかどうかを確認するのにフォーム オブジェクトは、DELETE_IS_MOVE フラグが返されたかどうかを決定する[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="1488b-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1488b-122">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="1488b-122">Notes to implementers</span></span>

<span data-ttu-id="1488b-123">**DeleteMessage**メソッドの実装をフォームのビューアーの移動する場合、次のメッセージのメッセージを削除した後、実装する必要があります[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)メソッドを呼び出すし、実行する前に VCDIR_DELETE フラグを渡す実際の削除します。</span><span class="sxs-lookup"><span data-stu-id="1488b-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="1488b-124">**DeleteMessage**フォーム ビューアーの実装では、(たとえば、 **[削除済みアイテム**フォルダー) に削除されたメッセージを移動した場合実装は、メッセージが変更された場合は、メッセージに変更を保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1488b-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="1488b-125">**DeleteMessage**の一般的な実装では、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="1488b-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="1488b-126">実装では、メッセージを移動では場合、は、 **null** _pMessage_パラメーターとの**場合は true** 、 _fSameAsLoad_パラメーターに渡して、 [IPersistMessage::Save](ipersistmessage-save.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1488b-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="1488b-127">_UlDir_パラメーターに VCDIR_DELETE フラグを渡す、 **IMAPIViewContext::ActivateNext**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1488b-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="1488b-128">**ActivateNext**の呼び出しが失敗したかどうかを返します。</span><span class="sxs-lookup"><span data-stu-id="1488b-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="1488b-129">**ActivateNext**が S_FALSE を返す場合は、 [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1488b-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="1488b-130">削除または、メッセージを移動します。</span><span class="sxs-lookup"><span data-stu-id="1488b-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="1488b-131">フォームのウィンドウで使用されている**RECT**構造体を取得するには、Windows[ハンドル](http://msdn.microsoft.com/en-us/library/ms633519)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1488b-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) function.</span></span> 
  
<span data-ttu-id="1488b-132">フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1488b-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1488b-133">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="1488b-133">MFCMAPI reference</span></span>

<span data-ttu-id="1488b-134">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="1488b-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1488b-135">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="1488b-135">**File**</span></span>|<span data-ttu-id="1488b-136">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="1488b-136">**Function**</span></span>|<span data-ttu-id="1488b-137">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="1488b-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1488b-138">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="1488b-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="1488b-139">CMyMAPIFormViewer::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="1488b-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="1488b-140">実装されていません。</span><span class="sxs-lookup"><span data-stu-id="1488b-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1488b-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="1488b-141">See also</span></span>



[<span data-ttu-id="1488b-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="1488b-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="1488b-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="1488b-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="1488b-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="1488b-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="1488b-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="1488b-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="1488b-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1488b-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="1488b-147">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1488b-147">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="1488b-148">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1488b-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

