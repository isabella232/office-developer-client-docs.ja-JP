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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412528"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="57a96-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="57a96-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="57a96-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57a96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57a96-105">フォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="57a96-105">Displays a form.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="57a96-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="57a96-106">Parameters</span></span>

 <span data-ttu-id="57a96-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="57a96-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="57a96-108">[in]フォームの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="57a96-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="57a96-109">_lpMsgStore_</span><span class="sxs-lookup"><span data-stu-id="57a96-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="57a96-110">[in]  _lpParentFolder_ パラメーターが指すフォルダーを含むメッセージ ストアへのポインター。</span><span class="sxs-lookup"><span data-stu-id="57a96-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="57a96-111">_lpParentFolder_</span><span class="sxs-lookup"><span data-stu-id="57a96-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="57a96-112">[in]  _ulMessageToken_ パラメーターに関連付けられたメッセージが作成されたフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="57a96-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="57a96-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="57a96-113">_lpInterface_</span></span>
  
> <span data-ttu-id="57a96-114">[in]フォームに表示されるメッセージにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="57a96-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="57a96-115">_lpInterface パラメーターは_ NULL または null IID_IMessage。</span><span class="sxs-lookup"><span data-stu-id="57a96-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="57a96-116">NULL を渡す場合、標準インターフェイス [IMessage](imessageimapiprop.md)が使用されます。</span><span class="sxs-lookup"><span data-stu-id="57a96-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="57a96-117">_ulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="57a96-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="57a96-118">[in]フォームに表示するメッセージに関連付けられているトークン。</span><span class="sxs-lookup"><span data-stu-id="57a96-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="57a96-119">_ulMessageToken_ パラメーターは、前の呼び出しから [IMAPISession::P repareForm](imapisession-prepareform.md)への _lpulMessageToken_ パラメーターの内容に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57a96-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="57a96-120">_lpMessageSent_</span><span class="sxs-lookup"><span data-stu-id="57a96-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="57a96-121">[in]予約済み。NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="57a96-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="57a96-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="57a96-122">_ulFlags_</span></span>
  
> <span data-ttu-id="57a96-123">[in]メッセージの保存方法と保存方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="57a96-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="57a96-124">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="57a96-124">The following flags can be set:</span></span>
    
<span data-ttu-id="57a96-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="57a96-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="57a96-126">メッセージが保存されたことがない ( [つまり、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドが呼び出されたことがない)。</span><span class="sxs-lookup"><span data-stu-id="57a96-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="57a96-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="57a96-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="57a96-128">メッセージは親フォルダーに保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57a96-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="57a96-129">メッセージは送信用に処理されませんが、代わりにフォルダーに投稿されます。</span><span class="sxs-lookup"><span data-stu-id="57a96-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="57a96-130">このフラグが設定されていない場合、メッセージは送信ボックスにコピーされ、送信用に処理されます。</span><span class="sxs-lookup"><span data-stu-id="57a96-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="57a96-131">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="57a96-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="57a96-132">[in]_ulMessageToken_ パラメーター内のトークンに **関連付けられた** メッセージの PR_MSG_STATUS ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされたフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="57a96-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="57a96-133">フラグは、メッセージの状態に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="57a96-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="57a96-134">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="57a96-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="57a96-135">[in]_ulMessageToken_ パラメーター内のトークン **に関連付** けられているメッセージの PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="57a96-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="57a96-136">これらのフラグは、メッセージの状態に関する詳細な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="57a96-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="57a96-137">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="57a96-137">_ulAccess_</span></span>
  
> <span data-ttu-id="57a96-138">[in]フォームに表示されるメッセージのアクセス許可レベルを示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="57a96-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="57a96-139">この情報は _、ulMessageToken_ パラメーター **PR_ACCESS** に関連付けられたメッセージの PR_ACCESS ([PidTagAccess](pidtagaccess-canonical-property.md)) プロパティからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="57a96-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="57a96-140">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="57a96-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="57a96-141">[in]_ulMessageToken_ パラメーター内のトークンに関連付けられたメッセージの **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティからコピーされた、フォームに表示されるメッセージのメッセージ クラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="57a96-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="57a96-142">戻り値</span><span class="sxs-lookup"><span data-stu-id="57a96-142">Return value</span></span>

<span data-ttu-id="57a96-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="57a96-143">S_OK</span></span> 
  
> <span data-ttu-id="57a96-144">フォームが正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="57a96-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="57a96-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="57a96-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="57a96-146">通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="57a96-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="57a96-147">注釈</span><span class="sxs-lookup"><span data-stu-id="57a96-147">Remarks</span></span>

<span data-ttu-id="57a96-148">**IMAPISession::ShowForm** メソッドは **、IMAPISession::P repareForm** メソッドによって準備されたメッセージ フォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="57a96-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="57a96-149">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="57a96-149">Notes to callers</span></span>

<span data-ttu-id="57a96-150">PrepareForm メソッドの _lpMessage_ パラメーターで渡されるメッセージへの参照は **1** つのみです。</span><span class="sxs-lookup"><span data-stu-id="57a96-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="57a96-151">フォームの実装では、MAPI で文書化されているエラー値以外のエラー値を返す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="57a96-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="57a96-152">これらのエラー値を使用してエラー状態をより正確に判断できる場合は、これを行います。</span><span class="sxs-lookup"><span data-stu-id="57a96-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="57a96-153">それ以外の場合は、これらのエラーを処理する場合と同じようにMAPI_E_CALL_FAILED。</span><span class="sxs-lookup"><span data-stu-id="57a96-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="57a96-154">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="57a96-154">MFCMAPI reference</span></span>

<span data-ttu-id="57a96-155">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57a96-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="57a96-156">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="57a96-156">**File**</span></span>|<span data-ttu-id="57a96-157">**関数**</span><span class="sxs-lookup"><span data-stu-id="57a96-157">**Function**</span></span>|<span data-ttu-id="57a96-158">**コメント**</span><span class="sxs-lookup"><span data-stu-id="57a96-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="57a96-159">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="57a96-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="57a96-160">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="57a96-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="57a96-161">MFCMAPI は **IMAPISession::ShowForm** メソッドを **PrepareForm** メソッドと共に使用して、モーダル 形式でメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="57a96-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57a96-162">関連項目</span><span class="sxs-lookup"><span data-stu-id="57a96-162">See also</span></span>



[<span data-ttu-id="57a96-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="57a96-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="57a96-164">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="57a96-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="57a96-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="57a96-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="57a96-166">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="57a96-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="57a96-167">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="57a96-167">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

