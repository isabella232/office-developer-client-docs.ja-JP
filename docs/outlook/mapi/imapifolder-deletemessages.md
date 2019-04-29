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
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="ebf3a-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="ebf3a-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="ebf3a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebf3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebf3a-105">1つまたは複数のメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ebf3a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ebf3a-106">Parameters</span></span>

 <span data-ttu-id="ebf3a-107">_lpmsglist_</span><span class="sxs-lookup"><span data-stu-id="ebf3a-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="ebf3a-108">順番削除するメッセージ数、およびメッセージを識別する[ENTRYID](entryid.md)構造体の配列を含む[entrylist](entrylist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="ebf3a-109">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="ebf3a-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="ebf3a-110">順番進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="ebf3a-111">_uluiparam_パラメーターは、 _ulflags_パラメーターで MESSAGE_DIALOG フラグが設定されていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="ebf3a-112">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="ebf3a-112">_lpProgress_</span></span>
  
> <span data-ttu-id="ebf3a-113">順番進行状況インジケーターを表示する progress オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="ebf3a-114">_lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="ebf3a-115">MESSAGE_DIALOG フラグが_ulflags_パラメーターで設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="ebf3a-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ebf3a-116">_ulFlags_</span></span>
  
> <span data-ttu-id="ebf3a-117">順番メッセージを削除する方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="ebf3a-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-118">The following flags can be set:</span></span>
    
<span data-ttu-id="ebf3a-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="ebf3a-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="ebf3a-120">削除されたものを含むすべてのメッセージを完全に削除します。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="ebf3a-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ebf3a-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="ebf3a-122">操作の進行状況を示すインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ebf3a-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="ebf3a-123">Return value</span></span>

<span data-ttu-id="ebf3a-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="ebf3a-124">S_OK</span></span> 
  
> <span data-ttu-id="ebf3a-125">指定したメッセージまたはメッセージが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="ebf3a-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="ebf3a-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="ebf3a-127">呼び出しは成功しましたが、すべてのメッセージが正常に削除されませんでした。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="ebf3a-128">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="ebf3a-129">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="ebf3a-130">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ebf3a-131">注釈</span><span class="sxs-lookup"><span data-stu-id="ebf3a-131">Remarks</span></span>

<span data-ttu-id="ebf3a-132">**imapifolder::D eletemessages**メソッドは、フォルダーからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="ebf3a-133">存在しないメッセージ、他の場所に移動したメッセージ、読み取り/書き込みアクセス許可で開いているメッセージ、または現在送信されているメッセージは削除できません。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ebf3a-134">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="ebf3a-134">Notes to implementers</span></span>

<span data-ttu-id="ebf3a-135">削除操作に複数のメッセージが含まれている場合は、1つ以上のメッセージを削除できない場合でも、フォルダーごとにできるだけ完全に操作を実行してください。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="ebf3a-136">メモリが不足している、ディスクの空き領域が不足している、メッセージストアが破損しているなど、操作を途中で停止しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ebf3a-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ebf3a-137">Notes to callers</span></span>

<span data-ttu-id="ebf3a-138">これらの戻り値は、次の条件に当てはまることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="ebf3a-139">**Condition**</span><span class="sxs-lookup"><span data-stu-id="ebf3a-139">**Condition**</span></span>|<span data-ttu-id="ebf3a-140">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="ebf3a-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ebf3a-141">**DeleteMessages**はすべてのメッセージを正常に削除しました。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="ebf3a-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="ebf3a-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="ebf3a-143">**DeleteMessages**は、すべてのメッセージとサブフォルダーを正常に削除できませんでした。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="ebf3a-144">MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ebf3a-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="ebf3a-145">**DeleteMessages**を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="ebf3a-146">MAPI_E_NOT_FOUND を除くすべてのエラー値</span><span class="sxs-lookup"><span data-stu-id="ebf3a-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="ebf3a-147">**DeleteMessages**が完了できない場合は、作業が行われていないことを前提としていません。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="ebf3a-148">エラーが発生する前に、 **DeleteMessages**は1つ以上のメッセージを削除できた可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="ebf3a-149">**DeleteMessages**は、メッセージストアの実装に応じて、MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ebf3a-150">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="ebf3a-150">MFCMAPI reference</span></span>

<span data-ttu-id="ebf3a-151">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ebf3a-152">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="ebf3a-152">**File**</span></span>|<span data-ttu-id="ebf3a-153">**関数**</span><span class="sxs-lookup"><span data-stu-id="ebf3a-153">**Function**</span></span>|<span data-ttu-id="ebf3a-154">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ebf3a-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ebf3a-155">folderdlg</span><span class="sxs-lookup"><span data-stu-id="ebf3a-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="ebf3a-156">cfolderdlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="ebf3a-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="ebf3a-157">mfcmapi は、 **imapifolder::D eletemessages**メソッドを使用して、指定されたメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="ebf3a-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ebf3a-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="ebf3a-158">See also</span></span>



[<span data-ttu-id="ebf3a-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ebf3a-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="ebf3a-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="ebf3a-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="ebf3a-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ebf3a-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="ebf3a-162">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ebf3a-162">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="ebf3a-163">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="ebf3a-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

