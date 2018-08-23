---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e9e0ad958acc40dd28f3d9aab9996c1b7a36f38a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591486"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="4290f-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="4290f-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="4290f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4290f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4290f-105">フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4290f-105">Displays a form.</span></span>
  
```cpp
HRESULT ShowForm(
  ULONG_PTR ulUIParam,
  LPMDB lpMsgStore,
  LPMAPIFOLDER lpParentFolder,
  LPCIID lpInterface,
  ULONG ulMessageToken,
  LPMESSAGE lpMessageSent,
  ULONG ulFlags,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  ULONG ulAccess,
  LPSTR lpszMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="4290f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4290f-106">Parameters</span></span>

 <span data-ttu-id="4290f-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4290f-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="4290f-108">[in]フォームの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="4290f-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="4290f-109">_lpMsgStore_</span><span class="sxs-lookup"><span data-stu-id="4290f-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="4290f-110">[in]_LpParentFolder_パラメーターが指すフォルダーが含まれるメッセージ ・ ストアへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="4290f-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="4290f-111">_lpParentFolder_</span><span class="sxs-lookup"><span data-stu-id="4290f-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="4290f-112">[in]_UlMessageToken_パラメーターに関連付けられているメッセージが作成されたフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4290f-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="4290f-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4290f-113">_lpInterface_</span></span>
  
> <span data-ttu-id="4290f-114">[in]フォームに表示されるメッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4290f-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="4290f-115">_LpInterface_パラメーターは、NULL または IID_IMessage である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4290f-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="4290f-116">NULL を渡すことは、標準的なインタ フェース、 [IMessage](imessageimapiprop.md)、使用中になります。</span><span class="sxs-lookup"><span data-stu-id="4290f-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="4290f-117">_ulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="4290f-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="4290f-118">[in]フォームに表示されるメッセージに関連付けられているトークンです。</span><span class="sxs-lookup"><span data-stu-id="4290f-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="4290f-119">[IMAPISession::PrepareForm](imapisession-prepareform.md)の以前の呼び出しからは、 _lpulMessageToken_パラメーターの内容を_ulMessageToken_パラメーターを設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4290f-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="4290f-120">_lpMessageSent_</span><span class="sxs-lookup"><span data-stu-id="4290f-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="4290f-121">[in]予約されています。NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4290f-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="4290f-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4290f-122">_ulFlags_</span></span>
  
> <span data-ttu-id="4290f-123">[in]メッセージを保存する方法とするかどうかを制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="4290f-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="4290f-124">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="4290f-124">The following flags can be set:</span></span>
    
<span data-ttu-id="4290f-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="4290f-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="4290f-126">メッセージが保存されていない (つまり、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドはそのことはありませんが呼び出されました)。</span><span class="sxs-lookup"><span data-stu-id="4290f-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="4290f-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="4290f-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="4290f-128">メッセージは、その親フォルダーに保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4290f-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="4290f-129">メッセージを送信するのには処理されませんが、代わりに、フォルダーに投稿します。</span><span class="sxs-lookup"><span data-stu-id="4290f-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="4290f-130">このフラグが設定されていない場合メッセージが送信トレイにコピーされを送信するための処理します。</span><span class="sxs-lookup"><span data-stu-id="4290f-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="4290f-131">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="4290f-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="4290f-132">[in]_UlMessageToken_パラメーターのトークンに関連付けられたメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティからコピーしたフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="4290f-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="4290f-133">フラグは、メッセージの状態に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="4290f-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="4290f-134">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="4290f-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="4290f-135">[in]_UlMessageToken_パラメーターのトークンに関連付けられたメッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティからコピーしたフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="4290f-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="4290f-136">これらのフラグさらに、メッセージの状態に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="4290f-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="4290f-137">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="4290f-137">_ulAccess_</span></span>
  
> <span data-ttu-id="4290f-138">[in]フォームに表示されるメッセージのアクセス許可レベルを示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="4290f-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="4290f-139">この情報は、 _ulMessageToken_パラメーターのトークンに関連付けられたメッセージの ([PidTagAccess](pidtagaccess-canonical-property.md)) である**PR_ACCESS**プロパティからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="4290f-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="4290f-140">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="4290f-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="4290f-141">[in]**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) は、 _ulMessageToken_パラメーターのトークンに関連付けられているメッセージのコピーをフォームに表示されているメッセージのメッセージ クラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4290f-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4290f-142">�߂�l</span><span class="sxs-lookup"><span data-stu-id="4290f-142">Return value</span></span>

<span data-ttu-id="4290f-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="4290f-143">S_OK</span></span> 
  
> <span data-ttu-id="4290f-144">フォームが正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="4290f-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="4290f-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="4290f-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="4290f-146">ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="4290f-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4290f-147">注釈</span><span class="sxs-lookup"><span data-stu-id="4290f-147">Remarks</span></span>

<span data-ttu-id="4290f-148">**IMAPISession::ShowForm**メソッドには、 **IMAPISession::PrepareForm**メソッドによって準備されているメッセージ フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4290f-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4290f-149">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4290f-149">Notes to callers</span></span>

<span data-ttu-id="4290f-150">**PrepareForm**メソッドの_lpMessage_パラメーターで渡されたメッセージに対する単一の参照だけが必要です。</span><span class="sxs-lookup"><span data-stu-id="4290f-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="4290f-151">フォームの実装が MAPI によって記載されているものとは別のエラー値を返すことに注意します。</span><span class="sxs-lookup"><span data-stu-id="4290f-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="4290f-152">これらのエラー値を使用すると、エラー状態のより正確な判断を下すため、これの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="4290f-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="4290f-153">MAPI_E_CALL_FAILED とそれ以外の場合、これらのエラーを処理します。</span><span class="sxs-lookup"><span data-stu-id="4290f-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4290f-154">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="4290f-154">MFCMAPI reference</span></span>

<span data-ttu-id="4290f-155">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="4290f-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4290f-156">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="4290f-156">**File**</span></span>|<span data-ttu-id="4290f-157">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="4290f-157">**Function**</span></span>|<span data-ttu-id="4290f-158">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="4290f-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4290f-159">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="4290f-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="4290f-160">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="4290f-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="4290f-161">MFCMAPI では、モーダル形式でメッセージを表示するのには、 **PrepareForm**メソッドと**IMAPISession::ShowForm**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="4290f-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4290f-162">関連項目</span><span class="sxs-lookup"><span data-stu-id="4290f-162">See also</span></span>



[<span data-ttu-id="4290f-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="4290f-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="4290f-164">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4290f-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="4290f-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="4290f-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="4290f-166">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4290f-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="4290f-167">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="4290f-167">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

