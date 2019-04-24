---
title: imapisessionshowform
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
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335666"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="5c19d-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="5c19d-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="5c19d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c19d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c19d-105">フォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="5c19d-105">Displays a form.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="5c19d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5c19d-106">Parameters</span></span>

 <span data-ttu-id="5c19d-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="5c19d-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="5c19d-108">順番フォームの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="5c19d-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="5c19d-109">_lpmsgstore_</span><span class="sxs-lookup"><span data-stu-id="5c19d-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="5c19d-110">順番_lpparentfolder_パラメーターによって指定されたフォルダーを含むメッセージストアへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5c19d-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="5c19d-111">_lpparentfolder_</span><span class="sxs-lookup"><span data-stu-id="5c19d-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="5c19d-112">順番_ulmessagetoken_パラメーターに関連付けられたメッセージが作成されたフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5c19d-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="5c19d-113">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="5c19d-113">_lpInterface_</span></span>
  
> <span data-ttu-id="5c19d-114">順番フォームに表示されるメッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5c19d-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="5c19d-115">_lpinterface_パラメーターは、NULL または IID_IMessage である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c19d-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="5c19d-116">NULL 結果を標準インターフェイス[IMessage](imessageimapiprop.md)で使用します。</span><span class="sxs-lookup"><span data-stu-id="5c19d-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="5c19d-117">_ulmessagetoken_</span><span class="sxs-lookup"><span data-stu-id="5c19d-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="5c19d-118">順番フォームに表示されるメッセージに関連付けられているトークン。</span><span class="sxs-lookup"><span data-stu-id="5c19d-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="5c19d-119">_ulmessagetoken_パラメーターは、以前の imapisession への呼び出しの_lアウト messagetoken_パラメーターの内容に設定する必要があります。 [:P repareform](imapisession-prepareform.md)。</span><span class="sxs-lookup"><span data-stu-id="5c19d-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="5c19d-120">_lpメッセージ ent_</span><span class="sxs-lookup"><span data-stu-id="5c19d-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="5c19d-121">順番予約語NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c19d-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="5c19d-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5c19d-122">_ulFlags_</span></span>
  
> <span data-ttu-id="5c19d-123">順番メッセージを保存する方法と方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="5c19d-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="5c19d-124">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5c19d-124">The following flags can be set:</span></span>
    
<span data-ttu-id="5c19d-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="5c19d-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="5c19d-126">メッセージが一度も保存されていません (つまり、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されていない)。</span><span class="sxs-lookup"><span data-stu-id="5c19d-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="5c19d-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="5c19d-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="5c19d-128">メッセージは、親フォルダーに保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c19d-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="5c19d-129">メッセージは送信用に処理されませんが、代わりにフォルダーに投稿されます。</span><span class="sxs-lookup"><span data-stu-id="5c19d-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="5c19d-130">このフラグが設定されていない場合、メッセージは送信トレイにコピーされ、送信用に処理されます。</span><span class="sxs-lookup"><span data-stu-id="5c19d-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="5c19d-131">_ulmessagestatus_</span><span class="sxs-lookup"><span data-stu-id="5c19d-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="5c19d-132">順番_ulmessagetoken_パラメーターのトークンに関連付けられているメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされたフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="5c19d-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="5c19d-133">フラグは、メッセージの状態に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c19d-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="5c19d-134">_ulmessageflags_</span><span class="sxs-lookup"><span data-stu-id="5c19d-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="5c19d-135">順番_ulmessagetoken_パラメーターのトークンに関連付けられているメッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="5c19d-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="5c19d-136">これらのフラグは、メッセージの状態に関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c19d-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="5c19d-137">_ulaccess_</span><span class="sxs-lookup"><span data-stu-id="5c19d-137">_ulAccess_</span></span>
  
> <span data-ttu-id="5c19d-138">順番フォームに表示されるメッセージのアクセス許可レベルを示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="5c19d-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="5c19d-139">この情報は、 _ulmessagetoken_パラメーターのトークンに関連付けられているメッセージの**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) プロパティからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5c19d-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="5c19d-140">_lpszmessageclass_</span><span class="sxs-lookup"><span data-stu-id="5c19d-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="5c19d-141">順番フォームに表示されているメッセージのメッセージクラスへのポインター。 _ulmessagetoken_パラメーターのトークンに関連付けられているメッセージの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティからコピーします。</span><span class="sxs-lookup"><span data-stu-id="5c19d-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5c19d-142">戻り値</span><span class="sxs-lookup"><span data-stu-id="5c19d-142">Return value</span></span>

<span data-ttu-id="5c19d-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="5c19d-143">S_OK</span></span> 
  
> <span data-ttu-id="5c19d-144">フォームが正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="5c19d-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="5c19d-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="5c19d-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="5c19d-146">ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c19d-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5c19d-147">解説</span><span class="sxs-lookup"><span data-stu-id="5c19d-147">Remarks</span></span>

<span data-ttu-id="5c19d-148">**imapisession:: showform**メソッドは、 **imapisession::P repareform**メソッドによって準備されたメッセージフォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="5c19d-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5c19d-149">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5c19d-149">Notes to callers</span></span>

<span data-ttu-id="5c19d-150">**PrepareForm**メソッドの_lpmessage_パラメーターで渡されるメッセージへの参照は1つだけにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c19d-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="5c19d-151">フォーム実装は、MAPI で文書化されているもの以外のエラー値を返すことができることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5c19d-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="5c19d-152">これらのエラー値を使用して、エラー条件をより正確に判断できるようにする場合は、このようにします。</span><span class="sxs-lookup"><span data-stu-id="5c19d-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="5c19d-153">それ以外の場合は、MAPI_E_CALL_FAILED を処理するのと同様に、これらのエラーを処理します。</span><span class="sxs-lookup"><span data-stu-id="5c19d-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5c19d-154">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="5c19d-154">MFCMAPI reference</span></span>

<span data-ttu-id="5c19d-155">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c19d-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5c19d-156">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="5c19d-156">**File**</span></span>|<span data-ttu-id="5c19d-157">**関数**</span><span class="sxs-lookup"><span data-stu-id="5c19d-157">**Function**</span></span>|<span data-ttu-id="5c19d-158">**コメント**</span><span class="sxs-lookup"><span data-stu-id="5c19d-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5c19d-159">MAPIFormFunctions</span><span class="sxs-lookup"><span data-stu-id="5c19d-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="5c19d-160">openmessagemodal</span><span class="sxs-lookup"><span data-stu-id="5c19d-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="5c19d-161">mfcmapi は、 **imapisession:: showform**メソッドを**PrepareForm**メソッドと共に使用して、モーダルフォームにメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="5c19d-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c19d-162">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c19d-162">See also</span></span>



[<span data-ttu-id="5c19d-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="5c19d-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="5c19d-164">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5c19d-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="5c19d-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="5c19d-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="5c19d-166">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5c19d-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="5c19d-167">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="5c19d-167">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

