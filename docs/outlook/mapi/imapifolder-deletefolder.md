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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 15cf8ff7e282035ddff53565aa92e81e3886729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800470"
---
# <a name="imapifolderdeletefolder"></a><span data-ttu-id="9895d-103">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="9895d-103">IMAPIFolder::DeleteFolder</span></span>

  
  
<span data-ttu-id="9895d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9895d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9895d-105">サブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="9895d-105">Deletes a subfolder.</span></span>
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9895d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9895d-106">Parameters</span></span>

 <span data-ttu-id="9895d-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="9895d-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="9895d-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="9895d-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="9895d-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="9895d-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="9895d-110">[in]サブフォルダーを削除するには、エントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9895d-110">[in] A pointer to the entry identifier of the subfolder to delete.</span></span>
    
 <span data-ttu-id="9895d-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9895d-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="9895d-112">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="9895d-112">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="9895d-113">_UlFlags_パラメーターに FOLDER_DIALOG フラグが設定されていない限り、 _ulUIParam_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="9895d-113">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="9895d-114">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="9895d-114">_lpProgress_</span></span>
  
> <span data-ttu-id="9895d-115">[in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9895d-115">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="9895d-116">_LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="9895d-116">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="9895d-117">_UlFlags_に FOLDER_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="9895d-117">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="9895d-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9895d-118">_ulFlags_</span></span>
  
> <span data-ttu-id="9895d-119">[in]サブフォルダーの削除を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="9895d-119">[in] A bitmask of flags that controls the deletion of the subfolder.</span></span> <span data-ttu-id="9895d-120">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="9895d-120">The following flags can be set:</span></span>
    
<span data-ttu-id="9895d-121">DEL_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="9895d-121">DEL_FOLDERS</span></span> 
  
> <span data-ttu-id="9895d-122">_LpEntryID_で指定されたサブフォルダーのすべてのサブフォルダーを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9895d-122">All subfolders of the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="9895d-123">DEL_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="9895d-123">DEL_MESSAGES</span></span> 
  
> <span data-ttu-id="9895d-124">_LpEntryID_で指定されたサブフォルダー内のすべてのメッセージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9895d-124">All messages in the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="9895d-125">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9895d-125">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="9895d-126">操作の進行中に進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9895d-126">A progress indicator should be displayed while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9895d-127">�߂�l</span><span class="sxs-lookup"><span data-stu-id="9895d-127">Return value</span></span>

<span data-ttu-id="9895d-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="9895d-128">S_OK</span></span> 
  
> <span data-ttu-id="9895d-129">指定したフォルダーが削除されました。</span><span class="sxs-lookup"><span data-stu-id="9895d-129">The specified folder has been successfully deleted.</span></span>
    
<span data-ttu-id="9895d-130">MAPI_E_HAS_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="9895d-130">MAPI_E_HAS_FOLDERS</span></span> 
  
> <span data-ttu-id="9895d-131">削除されているサブフォルダーには、サブフォルダーが含まれていて、DEL_FOLDERS フラグが設定されませんでした。</span><span class="sxs-lookup"><span data-stu-id="9895d-131">The subfolder being deleted contains subfolders, and the DEL_FOLDERS flag was not set.</span></span> <span data-ttu-id="9895d-132">サブフォルダーは削除されませんでした。</span><span class="sxs-lookup"><span data-stu-id="9895d-132">The subfolders were not deleted.</span></span>
    
<span data-ttu-id="9895d-133">MAPI_E_HAS_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="9895d-133">MAPI_E_HAS_MESSAGES</span></span> 
  
> <span data-ttu-id="9895d-134">サブフォルダーを削除するには、メッセージが表示されて、DEL_MESSAGES フラグが設定されませんでした。</span><span class="sxs-lookup"><span data-stu-id="9895d-134">The subfolder being deleted contains messages, and the DEL_MESSAGES flag was not set.</span></span> <span data-ttu-id="9895d-135">サブフォルダーは削除されませんでした。</span><span class="sxs-lookup"><span data-stu-id="9895d-135">The subfolder was not deleted.</span></span>
    
<span data-ttu-id="9895d-136">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="9895d-136">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="9895d-137">呼び出しが成功したが、すべてのエントリが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="9895d-137">The call succeeded, but not all of the entries were successfully deleted.</span></span> <span data-ttu-id="9895d-138">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9895d-138">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="9895d-139">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="9895d-139">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="9895d-140">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9895d-140">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9895d-141">備考</span><span class="sxs-lookup"><span data-stu-id="9895d-141">Remarks</span></span>

<span data-ttu-id="9895d-142">**IMAPIFolder::DeleteFolder**メソッドでは、サブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="9895d-142">The **IMAPIFolder::DeleteFolder** method deletes a subfolder.</span></span> <span data-ttu-id="9895d-143">既定では、 **DeleteFolder**が空のフォルダーに対してのみ動作する使用することが、正常に空でないフォルダーに 2 つのフラグを設定することによって: DEL_FOLDERS と DEL_MESSAGES。</span><span class="sxs-lookup"><span data-stu-id="9895d-143">By default, **DeleteFolder** operates only on empty folders, but you can use it successfully on non-empty folders by setting two flags: DEL_FOLDERS and DEL_MESSAGES.</span></span> <span data-ttu-id="9895d-144">空のフォルダーまたは**DeleteFolder**の呼び出しに DEL_FOLDERS と DEL_MESSAGES の両方のフラグを設定するフォルダーのみを削除できます。</span><span class="sxs-lookup"><span data-stu-id="9895d-144">Only empty folders or folders that set both the DEL_FOLDERS and DEL_MESSAGES flags on the **DeleteFolder** call can be deleted.</span></span> <span data-ttu-id="9895d-145">DEL_FOLDERS により、すべてのフォルダー内のサブフォルダーを削除します。DEL_MESSAGES は、すべてのフォルダーのメッセージを削除するを有効にします。</span><span class="sxs-lookup"><span data-stu-id="9895d-145">DEL_FOLDERS enables all of the folder's subfolders to be removed; DEL_MESSAGES enables all of the folder's messages to be removed.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9895d-146">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="9895d-146">Notes to implementers</span></span>

<span data-ttu-id="9895d-147">削除操作には、複数のフォルダーが含まれているときに、できるだけ完全に各フォルダーの操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="9895d-147">When the delete operation involves more than one folder, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="9895d-148">削除するフォルダーのいずれかの場合があります存在しないかが移動またはコピー他の場所。</span><span class="sxs-lookup"><span data-stu-id="9895d-148">Sometimes one of the folders to be deleted does not exist or has been moved or copied elsewhere.</span></span> <span data-ttu-id="9895d-149">メモリが不足している、ディスク領域、またはメッセージ ・ ストア内の破損が不足しているなど、ユーザーが制御できない障害が発生した場合を除きは、処理の途中で操作を停止しません。</span><span class="sxs-lookup"><span data-stu-id="9895d-149">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="9895d-150">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="9895d-150">Notes to callers</span></span>

<span data-ttu-id="9895d-151">次の条件下で、これらの戻り値を期待してください。</span><span class="sxs-lookup"><span data-stu-id="9895d-151">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="9895d-152">**条件**</span><span class="sxs-lookup"><span data-stu-id="9895d-152">**Condition**</span></span>|<span data-ttu-id="9895d-153">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="9895d-153">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9895d-154">**DeleteFolder**は、すべてのメッセージとサブフォルダーが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="9895d-154">**DeleteFolder** has successfully deleted every message and subfolder.</span></span>  <br/> |<span data-ttu-id="9895d-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="9895d-155">S_OK</span></span>  <br/> |
|<span data-ttu-id="9895d-156">**DeleteFolder**は、正常にすべてのメッセージとサブフォルダーを削除できませんでした。</span><span class="sxs-lookup"><span data-stu-id="9895d-156">**DeleteFolder** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="9895d-157">MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9895d-157">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="9895d-158">**DeleteFolder**は完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="9895d-158">**DeleteFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="9895d-159">MAPI_E_NOT_FOUND を除くエラー値</span><span class="sxs-lookup"><span data-stu-id="9895d-159">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="9895d-160">**DeleteFolder**が完了することではない場合と仮定しないでその作業は実行されませんでした。</span><span class="sxs-lookup"><span data-stu-id="9895d-160">When **DeleteFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="9895d-161">**DeleteFolder**はエラーが発生する前に 1 つまたは複数のメッセージとサブフォルダーを削除することにされている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9895d-161">**DeleteFolder** might have been able to delete one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="9895d-162">1 つまたは複数のサブフォルダーを削除できない場合、 **DeleteFolder**は、メッセージ ストア プロバイダーの実装によって MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="9895d-162">If one or more subfolders cannot be deleted, **DeleteFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store provider's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9895d-163">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="9895d-163">MFCMAPI reference</span></span>

<span data-ttu-id="9895d-164">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="9895d-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9895d-165">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="9895d-165">**File**</span></span>|<span data-ttu-id="9895d-166">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="9895d-166">**Function**</span></span>|<span data-ttu-id="9895d-167">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="9895d-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9895d-168">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9895d-168">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="9895d-169">CMsgStoreDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="9895d-169">CMsgStoreDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="9895d-170">MFCMAPI では、 **IMAPIFolder::DeleteFolder**メソッドを使用して、フォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="9895d-170">MFCMAPI uses the **IMAPIFolder::DeleteFolder** method to delete folders.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9895d-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="9895d-171">See also</span></span>



[<span data-ttu-id="9895d-172">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="9895d-172">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="9895d-173">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="9895d-173">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

