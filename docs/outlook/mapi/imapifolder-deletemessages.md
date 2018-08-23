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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7845abc4f3010daf8e13d56ac4b13d0333bad07e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800491"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="0e5e6-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="0e5e6-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="0e5e6-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e5e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e5e6-105">1 つまたは複数のメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0e5e6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e5e6-106">Parameters</span></span>

 <span data-ttu-id="0e5e6-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="0e5e6-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="0e5e6-108">[in]削除するメッセージの数と、メッセージを識別する[エントリ ID](entryid.md)の構造体の配列を含む[ENTRYLIST](entrylist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="0e5e6-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0e5e6-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="0e5e6-110">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="0e5e6-111">_UlFlags_パラメーターに MESSAGE_DIALOG フラグが設定されていない限り、 _ulUIParam_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="0e5e6-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="0e5e6-112">_lpProgress_</span></span>
  
> <span data-ttu-id="0e5e6-113">[in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="0e5e6-114">_LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="0e5e6-115">_UlFlags_パラメーターに MESSAGE_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="0e5e6-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0e5e6-116">_ulFlags_</span></span>
  
> <span data-ttu-id="0e5e6-117">[in]メッセージを削除する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="0e5e6-118">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-118">The following flags can be set:</span></span>
    
<span data-ttu-id="0e5e6-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="0e5e6-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="0e5e6-120">ソフト削除されたものも含めて、すべてのメッセージを完全に削除します。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="0e5e6-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="0e5e6-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="0e5e6-122">操作の進行中は、進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0e5e6-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0e5e6-123">Return value</span></span>

<span data-ttu-id="0e5e6-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e5e6-124">S_OK</span></span> 
  
> <span data-ttu-id="0e5e6-125">指定したメッセージまたはメッセージが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="0e5e6-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="0e5e6-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="0e5e6-127">呼び出しが成功したが、すべてのメッセージが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="0e5e6-128">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="0e5e6-129">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="0e5e6-130">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e5e6-131">注釈</span><span class="sxs-lookup"><span data-stu-id="0e5e6-131">Remarks</span></span>

<span data-ttu-id="0e5e6-132">**IMAPIFolder::DeleteMessages**メソッドは、フォルダーからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="0e5e6-133">存在せず、別の場所に移動されている、読み取り/書き込み権限で開かれている、または送信される現在のメッセージを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0e5e6-134">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="0e5e6-134">Notes to implementers</span></span>

<span data-ttu-id="0e5e6-135">削除操作には、複数のメッセージが含まれているときに操作を実行できるだけ完全に、フォルダーごとに 1 つまたは複数のメッセージを削除できない場合でも。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="0e5e6-136">メモリが不足している、ディスク領域、またはメッセージ ・ ストア内の破損が不足しているなど、ユーザーが制御できない障害が発生した場合を除きは、処理の途中で操作を停止しません。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="0e5e6-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="0e5e6-137">Notes to callers</span></span>

<span data-ttu-id="0e5e6-138">次の条件下で、これらの戻り値を期待してください。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="0e5e6-139">**条件**</span><span class="sxs-lookup"><span data-stu-id="0e5e6-139">**Condition**</span></span>|<span data-ttu-id="0e5e6-140">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="0e5e6-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0e5e6-141">**DeleteMessages**はすべてのメッセージを正常に削除します。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="0e5e6-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e5e6-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="0e5e6-143">**DeleteMessages**は、正常にすべてのメッセージとサブフォルダーを削除できませんでした。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="0e5e6-144">MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0e5e6-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="0e5e6-145">**DeleteMessages**は完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="0e5e6-146">MAPI_E_NOT_FOUND を除くエラー値</span><span class="sxs-lookup"><span data-stu-id="0e5e6-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="0e5e6-147">**DeleteMessages**が完了することではない場合と仮定しないでその作業は実行されませんでした。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="0e5e6-148">**DeleteMessages**はエラーが発生する前に 1 つまたは複数のメッセージを削除することにされている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="0e5e6-149">**DeleteMessages**は、メッセージ ストアの実装によって、MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0e5e6-150">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="0e5e6-150">MFCMAPI reference</span></span>

<span data-ttu-id="0e5e6-151">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="0e5e6-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0e5e6-152">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="0e5e6-152">**File**</span></span>|<span data-ttu-id="0e5e6-153">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="0e5e6-153">**Function**</span></span>|<span data-ttu-id="0e5e6-154">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="0e5e6-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e5e6-155">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0e5e6-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="0e5e6-156">CFolderDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="0e5e6-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="0e5e6-157">MFCMAPI では、 **IMAPIFolder::DeleteMessages**メソッドを使用して、指定したメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="0e5e6-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e5e6-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="0e5e6-158">See also</span></span>



[<span data-ttu-id="0e5e6-159">エントリ ID</span><span class="sxs-lookup"><span data-stu-id="0e5e6-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="0e5e6-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="0e5e6-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="0e5e6-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0e5e6-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="0e5e6-162">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="0e5e6-162">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="0e5e6-163">エラー処理のためのマクロの使用</span><span class="sxs-lookup"><span data-stu-id="0e5e6-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

