---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417407"
---
# <a name="imapifolderdeletefolder"></a><span data-ttu-id="f5f63-103">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="f5f63-103">IMAPIFolder::DeleteFolder</span></span>

  
  
<span data-ttu-id="f5f63-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5f63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5f63-105">サブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="f5f63-105">Deletes a subfolder.</span></span>
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f5f63-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f5f63-106">Parameters</span></span>

 <span data-ttu-id="f5f63-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f5f63-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f5f63-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="f5f63-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f5f63-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f5f63-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f5f63-110">[in]削除するサブフォルダーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f5f63-110">[in] A pointer to the entry identifier of the subfolder to delete.</span></span>
    
 <span data-ttu-id="f5f63-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f5f63-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="f5f63-112">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="f5f63-112">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="f5f63-113">_ulUIParam_ パラメーターは _、ulFlags_ パラメーター FOLDER_DIALOGフラグが設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="f5f63-113">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f5f63-114">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="f5f63-114">_lpProgress_</span></span>
  
> <span data-ttu-id="f5f63-115">[in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f5f63-115">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="f5f63-116">_lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="f5f63-116">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="f5f63-117">_lpProgress パラメーター_ は _、ulFlags_ で FOLDER_DIALOGフラグが設定されていない限り無視されます。</span><span class="sxs-lookup"><span data-stu-id="f5f63-117">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="f5f63-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f5f63-118">_ulFlags_</span></span>
  
> <span data-ttu-id="f5f63-119">[in]サブフォルダーの削除を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f5f63-119">[in] A bitmask of flags that controls the deletion of the subfolder.</span></span> <span data-ttu-id="f5f63-120">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f5f63-120">The following flags can be set:</span></span>
    
<span data-ttu-id="f5f63-121">DEL_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="f5f63-121">DEL_FOLDERS</span></span> 
  
> <span data-ttu-id="f5f63-122">_lpEntryID_ が指すサブフォルダーのすべてのサブフォルダーを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5f63-122">All subfolders of the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="f5f63-123">DEL_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="f5f63-123">DEL_MESSAGES</span></span> 
  
> <span data-ttu-id="f5f63-124">_lpEntryID_ が指すサブフォルダー内のすべてのメッセージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5f63-124">All messages in the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="f5f63-125">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f5f63-125">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="f5f63-126">操作の進行中に進行状況インジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f5f63-126">A progress indicator should be displayed while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f5f63-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="f5f63-127">Return value</span></span>

<span data-ttu-id="f5f63-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5f63-128">S_OK</span></span> 
  
> <span data-ttu-id="f5f63-129">指定したフォルダーが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="f5f63-129">The specified folder has been successfully deleted.</span></span>
    
<span data-ttu-id="f5f63-130">MAPI_E_HAS_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="f5f63-130">MAPI_E_HAS_FOLDERS</span></span> 
  
> <span data-ttu-id="f5f63-131">削除されるサブフォルダーにはサブフォルダーが含まれているので、DEL_FOLDERSフラグは設定されません。</span><span class="sxs-lookup"><span data-stu-id="f5f63-131">The subfolder being deleted contains subfolders, and the DEL_FOLDERS flag was not set.</span></span> <span data-ttu-id="f5f63-132">サブフォルダーは削除されません。</span><span class="sxs-lookup"><span data-stu-id="f5f63-132">The subfolders were not deleted.</span></span>
    
<span data-ttu-id="f5f63-133">MAPI_E_HAS_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="f5f63-133">MAPI_E_HAS_MESSAGES</span></span> 
  
> <span data-ttu-id="f5f63-134">削除されるサブフォルダーにはメッセージが含まれますが、DEL_MESSAGESフラグは設定されません。</span><span class="sxs-lookup"><span data-stu-id="f5f63-134">The subfolder being deleted contains messages, and the DEL_MESSAGES flag was not set.</span></span> <span data-ttu-id="f5f63-135">サブフォルダーは削除されません。</span><span class="sxs-lookup"><span data-stu-id="f5f63-135">The subfolder was not deleted.</span></span>
    
<span data-ttu-id="f5f63-136">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="f5f63-136">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="f5f63-137">呼び出しは成功しましたが、すべてのエントリが正常に削除されたという訳ではありません。</span><span class="sxs-lookup"><span data-stu-id="f5f63-137">The call succeeded, but not all of the entries were successfully deleted.</span></span> <span data-ttu-id="f5f63-138">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="f5f63-138">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="f5f63-139">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="f5f63-139">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="f5f63-140">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="f5f63-140">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f5f63-141">注釈</span><span class="sxs-lookup"><span data-stu-id="f5f63-141">Remarks</span></span>

<span data-ttu-id="f5f63-142">**IMAPIFolder::D eleteFolder メソッドは** サブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="f5f63-142">The **IMAPIFolder::DeleteFolder** method deletes a subfolder.</span></span> <span data-ttu-id="f5f63-143">既定では **、DeleteFolder** は空のフォルダーでのみ動作しますが、空でないフォルダーでは、DEL_FOLDERS と DEL_MESSAGES の 2 つのフラグを設定することで、このフォルダーを正常に使用できます。</span><span class="sxs-lookup"><span data-stu-id="f5f63-143">By default, **DeleteFolder** operates only on empty folders, but you can use it successfully on non-empty folders by setting two flags: DEL_FOLDERS and DEL_MESSAGES.</span></span> <span data-ttu-id="f5f63-144">**DeleteFolder** 呼び出しでDEL_FOLDERSとDEL_MESSAGES両方を設定する空のフォルダーまたはフォルダーのみを削除できます。</span><span class="sxs-lookup"><span data-stu-id="f5f63-144">Only empty folders or folders that set both the DEL_FOLDERS and DEL_MESSAGES flags on the **DeleteFolder** call can be deleted.</span></span> <span data-ttu-id="f5f63-145">DEL_FOLDERSフォルダーのすべてのサブフォルダーを削除できます。DEL_MESSAGESフォルダーのすべてのメッセージを削除できます。</span><span class="sxs-lookup"><span data-stu-id="f5f63-145">DEL_FOLDERS enables all of the folder's subfolders to be removed; DEL_MESSAGES enables all of the folder's messages to be removed.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f5f63-146">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="f5f63-146">Notes to implementers</span></span>

<span data-ttu-id="f5f63-147">削除操作に複数のフォルダーが含まれる場合は、フォルダーごとに可能な限り完全に操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="f5f63-147">When the delete operation involves more than one folder, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="f5f63-148">削除するフォルダーの 1 つが存在しないか、他の場所に移動またはコピーされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="f5f63-148">Sometimes one of the folders to be deleted does not exist or has been moved or copied elsewhere.</span></span> <span data-ttu-id="f5f63-149">メモリの使い切れ、ディスク領域の使い切れ、メッセージ ストアの破損など、制御できないエラーが発生しない限り、操作を途中で停止しません。</span><span class="sxs-lookup"><span data-stu-id="f5f63-149">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f5f63-150">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f5f63-150">Notes to callers</span></span>

<span data-ttu-id="f5f63-151">これらの戻り値は、次の条件下で期待してください。</span><span class="sxs-lookup"><span data-stu-id="f5f63-151">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="f5f63-152">**Condition**</span><span class="sxs-lookup"><span data-stu-id="f5f63-152">**Condition**</span></span>|<span data-ttu-id="f5f63-153">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="f5f63-153">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5f63-154">**DeleteFolder は** 、すべてのメッセージとサブフォルダーを正常に削除しました。</span><span class="sxs-lookup"><span data-stu-id="f5f63-154">**DeleteFolder** has successfully deleted every message and subfolder.</span></span>  <br/> |<span data-ttu-id="f5f63-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5f63-155">S_OK</span></span>  <br/> |
|<span data-ttu-id="f5f63-156">**DeleteFolder** は、すべてのメッセージとサブフォルダーを正常に削除できなかった。</span><span class="sxs-lookup"><span data-stu-id="f5f63-156">**DeleteFolder** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="f5f63-157">MAPI_W_PARTIAL_COMPLETIONまたはMAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f5f63-157">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="f5f63-158">**DeleteFolder** を完了できなかった。</span><span class="sxs-lookup"><span data-stu-id="f5f63-158">**DeleteFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="f5f63-159">エラー以外のエラー MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f5f63-159">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="f5f63-160">**DeleteFolder を** 完了できない場合は、作業が完了していないと見なす必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f5f63-160">When **DeleteFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="f5f63-161">**DeleteFolder は** 、エラーが発生する前に 1 つ以上のメッセージとサブフォルダーを削除できた可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f5f63-161">**DeleteFolder** might have been able to delete one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="f5f63-162">1 つ以上のサブフォルダーを削除できない場合 **、DeleteFolder** はメッセージ ストア プロバイダーの実装に応じて、MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="f5f63-162">If one or more subfolders cannot be deleted, **DeleteFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store provider's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f5f63-163">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="f5f63-163">MFCMAPI reference</span></span>

<span data-ttu-id="f5f63-164">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f5f63-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f5f63-165">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="f5f63-165">**File**</span></span>|<span data-ttu-id="f5f63-166">**関数**</span><span class="sxs-lookup"><span data-stu-id="f5f63-166">**Function**</span></span>|<span data-ttu-id="f5f63-167">**コメント**</span><span class="sxs-lookup"><span data-stu-id="f5f63-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f5f63-168">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f5f63-168">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="f5f63-169">CMsgStoreDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="f5f63-169">CMsgStoreDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="f5f63-170">MFCMAPI は **IMAPIFolder::D eleteFolder** メソッドを使用してフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="f5f63-170">MFCMAPI uses the **IMAPIFolder::DeleteFolder** method to delete folders.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5f63-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5f63-171">See also</span></span>



[<span data-ttu-id="f5f63-172">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f5f63-172">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="f5f63-173">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="f5f63-173">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

