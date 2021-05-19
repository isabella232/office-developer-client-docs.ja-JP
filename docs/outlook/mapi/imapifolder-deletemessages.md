---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426073"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="f6103-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="f6103-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="f6103-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6103-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6103-105">1 つ以上のメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="f6103-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f6103-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f6103-106">Parameters</span></span>

 <span data-ttu-id="f6103-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="f6103-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="f6103-108">[in]削除するメッセージ [の数](entrylist.md) と、メッセージを識別する ENTRYID 構造体の配列を含む [ENTRYLIST](entryid.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f6103-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="f6103-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f6103-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="f6103-110">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="f6103-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="f6103-111">_ulUIParam_ パラメーターは _、ulFlags_ パラメーター MESSAGE_DIALOGフラグが設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="f6103-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f6103-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="f6103-112">_lpProgress_</span></span>
  
> <span data-ttu-id="f6103-113">[in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f6103-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="f6103-114">_lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="f6103-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="f6103-115">_lpProgress パラメーター_ は _、ulFlags_ パラメーター MESSAGE_DIALOGフラグが設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="f6103-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f6103-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f6103-116">_ulFlags_</span></span>
  
> <span data-ttu-id="f6103-117">[in]メッセージの削除方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f6103-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="f6103-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f6103-118">The following flags can be set:</span></span>
    
<span data-ttu-id="f6103-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="f6103-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="f6103-120">ソフト削除されたメッセージを含むすべてのメッセージを完全に削除します。</span><span class="sxs-lookup"><span data-stu-id="f6103-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="f6103-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f6103-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="f6103-122">操作が進むにつれて進行状況インジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6103-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f6103-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="f6103-123">Return value</span></span>

<span data-ttu-id="f6103-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6103-124">S_OK</span></span> 
  
> <span data-ttu-id="f6103-125">指定したメッセージまたはメッセージが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="f6103-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="f6103-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="f6103-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="f6103-127">呼び出しは成功しましたが、すべてのメッセージが正常に削除されたというのではありません。</span><span class="sxs-lookup"><span data-stu-id="f6103-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="f6103-128">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="f6103-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="f6103-129">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="f6103-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="f6103-130">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="f6103-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6103-131">注釈</span><span class="sxs-lookup"><span data-stu-id="f6103-131">Remarks</span></span>

<span data-ttu-id="f6103-132">**IMAPIFolder::D eleteMessages** メソッドは、フォルダーからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="f6103-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="f6103-133">存在しないメッセージ、他の場所に移動されたメッセージ、読み取り/書き込み権限で開いているメッセージ、または現在送信されているメッセージは削除できません。</span><span class="sxs-lookup"><span data-stu-id="f6103-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f6103-134">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="f6103-134">Notes to implementers</span></span>

<span data-ttu-id="f6103-135">削除操作に複数のメッセージが含まれる場合は、1 つ以上のメッセージを削除できない場合でも、フォルダーごとに可能な限り完全に操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="f6103-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="f6103-136">メモリの使い切れ、ディスク領域の使い切れ、メッセージ ストアの破損など、制御できないエラーが発生しない限り、操作を途中で停止しません。</span><span class="sxs-lookup"><span data-stu-id="f6103-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f6103-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f6103-137">Notes to callers</span></span>

<span data-ttu-id="f6103-138">これらの戻り値は、次の条件下で期待してください。</span><span class="sxs-lookup"><span data-stu-id="f6103-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="f6103-139">**Condition**</span><span class="sxs-lookup"><span data-stu-id="f6103-139">**Condition**</span></span>|<span data-ttu-id="f6103-140">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="f6103-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f6103-141">**DeleteMessages は** 、すべてのメッセージを正常に削除しました。</span><span class="sxs-lookup"><span data-stu-id="f6103-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="f6103-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6103-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="f6103-143">**DeleteMessages は** 、すべてのメッセージとサブフォルダーを正常に削除できなかった。</span><span class="sxs-lookup"><span data-stu-id="f6103-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="f6103-144">MAPI_W_PARTIAL_COMPLETIONまたはMAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f6103-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="f6103-145">**DeleteMessages** を完了できません。</span><span class="sxs-lookup"><span data-stu-id="f6103-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="f6103-146">エラー以外のエラー MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f6103-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="f6103-147">**DeleteMessages を** 完了できない場合は、作業が完了していないと想定しません。</span><span class="sxs-lookup"><span data-stu-id="f6103-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="f6103-148">**DeleteMessages は** 、エラーが発生する前に 1 つ以上のメッセージを削除できた可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f6103-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="f6103-149">**DeleteMessages は** 、メッセージ MAPI_W_PARTIAL_COMPLETIONのMAPI_E_NOT_FOUNDに応じて、この値を返します。</span><span class="sxs-lookup"><span data-stu-id="f6103-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f6103-150">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="f6103-150">MFCMAPI reference</span></span>

<span data-ttu-id="f6103-151">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6103-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f6103-152">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="f6103-152">**File**</span></span>|<span data-ttu-id="f6103-153">**関数**</span><span class="sxs-lookup"><span data-stu-id="f6103-153">**Function**</span></span>|<span data-ttu-id="f6103-154">**コメント**</span><span class="sxs-lookup"><span data-stu-id="f6103-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6103-155">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f6103-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="f6103-156">CFolderDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="f6103-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="f6103-157">MFCMAPI は **IMAPIFolder::D eleteMessages** メソッドを使用して、指定したメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="f6103-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6103-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6103-158">See also</span></span>



[<span data-ttu-id="f6103-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f6103-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="f6103-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="f6103-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="f6103-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f6103-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="f6103-162">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="f6103-162">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="f6103-163">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="f6103-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

