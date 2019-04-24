---
title: imapifolderdeletefolder
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280072"
---
# <a name="imapifolderdeletefolder"></a><span data-ttu-id="798b9-103">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="798b9-103">IMAPIFolder::DeleteFolder</span></span>

  
  
<span data-ttu-id="798b9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="798b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="798b9-105">サブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="798b9-105">Deletes a subfolder.</span></span>
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="798b9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="798b9-106">Parameters</span></span>

 <span data-ttu-id="798b9-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="798b9-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="798b9-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="798b9-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="798b9-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="798b9-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="798b9-110">順番削除するサブフォルダーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="798b9-110">[in] A pointer to the entry identifier of the subfolder to delete.</span></span>
    
 <span data-ttu-id="798b9-111">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="798b9-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="798b9-112">順番進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="798b9-112">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="798b9-113">_uluiparam_パラメーターは、 _ulflags_パラメーターで FOLDER_DIALOG フラグが設定されていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="798b9-113">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="798b9-114">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="798b9-114">_lpProgress_</span></span>
  
> <span data-ttu-id="798b9-115">順番進行状況インジケーターを表示する progress オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="798b9-115">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="798b9-116">_lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="798b9-116">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="798b9-117">FOLDER_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="798b9-117">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="798b9-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="798b9-118">_ulFlags_</span></span>
  
> <span data-ttu-id="798b9-119">順番サブフォルダーの削除を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="798b9-119">[in] A bitmask of flags that controls the deletion of the subfolder.</span></span> <span data-ttu-id="798b9-120">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="798b9-120">The following flags can be set:</span></span>
    
<span data-ttu-id="798b9-121">DEL_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="798b9-121">DEL_FOLDERS</span></span> 
  
> <span data-ttu-id="798b9-122">_lな tryid_によって参照されるサブフォルダーのすべてのサブフォルダーを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="798b9-122">All subfolders of the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="798b9-123">DEL_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="798b9-123">DEL_MESSAGES</span></span> 
  
> <span data-ttu-id="798b9-124">_lな tryid_が指すサブフォルダー内のすべてのメッセージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="798b9-124">All messages in the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="798b9-125">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="798b9-125">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="798b9-126">操作の進行中に、進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="798b9-126">A progress indicator should be displayed while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="798b9-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="798b9-127">Return value</span></span>

<span data-ttu-id="798b9-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="798b9-128">S_OK</span></span> 
  
> <span data-ttu-id="798b9-129">指定したフォルダーが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="798b9-129">The specified folder has been successfully deleted.</span></span>
    
<span data-ttu-id="798b9-130">MAPI_E_HAS_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="798b9-130">MAPI_E_HAS_FOLDERS</span></span> 
  
> <span data-ttu-id="798b9-131">削除されるサブフォルダーにサブフォルダーが含まれており、DEL_FOLDERS フラグが設定されていません。</span><span class="sxs-lookup"><span data-stu-id="798b9-131">The subfolder being deleted contains subfolders, and the DEL_FOLDERS flag was not set.</span></span> <span data-ttu-id="798b9-132">サブフォルダーは削除されませんでした。</span><span class="sxs-lookup"><span data-stu-id="798b9-132">The subfolders were not deleted.</span></span>
    
<span data-ttu-id="798b9-133">MAPI_E_HAS_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="798b9-133">MAPI_E_HAS_MESSAGES</span></span> 
  
> <span data-ttu-id="798b9-134">削除されるサブフォルダーにメッセージが含まれており、DEL_MESSAGES フラグが設定されていませんでした。</span><span class="sxs-lookup"><span data-stu-id="798b9-134">The subfolder being deleted contains messages, and the DEL_MESSAGES flag was not set.</span></span> <span data-ttu-id="798b9-135">サブフォルダーは削除されませんでした。</span><span class="sxs-lookup"><span data-stu-id="798b9-135">The subfolder was not deleted.</span></span>
    
<span data-ttu-id="798b9-136">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="798b9-136">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="798b9-137">呼び出しは成功しましたが、すべてのエントリが正常に削除されませんでした。</span><span class="sxs-lookup"><span data-stu-id="798b9-137">The call succeeded, but not all of the entries were successfully deleted.</span></span> <span data-ttu-id="798b9-138">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="798b9-138">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="798b9-139">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="798b9-139">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="798b9-140">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="798b9-140">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="798b9-141">解説</span><span class="sxs-lookup"><span data-stu-id="798b9-141">Remarks</span></span>

<span data-ttu-id="798b9-142">**imapifolder::D eletefolder**メソッドは、サブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="798b9-142">The **IMAPIFolder::DeleteFolder** method deletes a subfolder.</span></span> <span data-ttu-id="798b9-143">既定では、 **deletefolder**は空のフォルダーでのみ動作しますが、DEL_FOLDERS と DEL_MESSAGES の2つのフラグを設定することにより、空ではないフォルダーで正常に使用できます。</span><span class="sxs-lookup"><span data-stu-id="798b9-143">By default, **DeleteFolder** operates only on empty folders, but you can use it successfully on non-empty folders by setting two flags: DEL_FOLDERS and DEL_MESSAGES.</span></span> <span data-ttu-id="798b9-144">**deletefolder**呼び出しで DEL_FOLDERS と DEL_MESSAGES の両方のフラグを設定する、空のフォルダーまたはフォルダーのみを削除できます。</span><span class="sxs-lookup"><span data-stu-id="798b9-144">Only empty folders or folders that set both the DEL_FOLDERS and DEL_MESSAGES flags on the **DeleteFolder** call can be deleted.</span></span> <span data-ttu-id="798b9-145">DEL_FOLDERS を使用すると、すべてのフォルダーのサブフォルダーを削除できます。DEL_MESSAGES を使用すると、フォルダーのすべてのメッセージを削除できます。</span><span class="sxs-lookup"><span data-stu-id="798b9-145">DEL_FOLDERS enables all of the folder's subfolders to be removed; DEL_MESSAGES enables all of the folder's messages to be removed.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="798b9-146">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="798b9-146">Notes to implementers</span></span>

<span data-ttu-id="798b9-147">削除操作に複数のフォルダーが含まれている場合は、各フォルダーで可能な限り完全に操作を実行してください。</span><span class="sxs-lookup"><span data-stu-id="798b9-147">When the delete operation involves more than one folder, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="798b9-148">削除するフォルダーの1つが存在しない場合や、他の場所に移動またはコピーされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="798b9-148">Sometimes one of the folders to be deleted does not exist or has been moved or copied elsewhere.</span></span> <span data-ttu-id="798b9-149">メモリが不足している、ディスクの空き領域が不足している、メッセージストアが破損しているなど、操作を途中で停止しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="798b9-149">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="798b9-150">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="798b9-150">Notes to callers</span></span>

<span data-ttu-id="798b9-151">これらの戻り値は、次の条件に当てはまることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="798b9-151">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="798b9-152">**Condition**</span><span class="sxs-lookup"><span data-stu-id="798b9-152">**Condition**</span></span>|<span data-ttu-id="798b9-153">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="798b9-153">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="798b9-154">**deletefolder**がすべてのメッセージとサブフォルダを正常に削除しました。</span><span class="sxs-lookup"><span data-stu-id="798b9-154">**DeleteFolder** has successfully deleted every message and subfolder.</span></span>  <br/> |<span data-ttu-id="798b9-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="798b9-155">S_OK</span></span>  <br/> |
|<span data-ttu-id="798b9-156">**deletefolder**は、すべてのメッセージとサブフォルダを正常に削除できませんでした。</span><span class="sxs-lookup"><span data-stu-id="798b9-156">**DeleteFolder** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="798b9-157">MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="798b9-157">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="798b9-158">**deletefolder**を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="798b9-158">**DeleteFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="798b9-159">MAPI_E_NOT_FOUND を除くすべてのエラー値</span><span class="sxs-lookup"><span data-stu-id="798b9-159">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="798b9-160">**deletefolder**を完了できない場合でも、作業が行われていないとは限りません。</span><span class="sxs-lookup"><span data-stu-id="798b9-160">When **DeleteFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="798b9-161">**deletefolder**がエラーが発生する前に、1つ以上のメッセージとサブフォルダーを削除できた可能性があります。</span><span class="sxs-lookup"><span data-stu-id="798b9-161">**DeleteFolder** might have been able to delete one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="798b9-162">1つまたは複数のサブフォルダーを削除できない場合、 **deletefolder**は、メッセージストアプロバイダーの実装に応じて MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="798b9-162">If one or more subfolders cannot be deleted, **DeleteFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store provider's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="798b9-163">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="798b9-163">MFCMAPI reference</span></span>

<span data-ttu-id="798b9-164">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="798b9-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="798b9-165">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="798b9-165">**File**</span></span>|<span data-ttu-id="798b9-166">**関数**</span><span class="sxs-lookup"><span data-stu-id="798b9-166">**Function**</span></span>|<span data-ttu-id="798b9-167">**コメント**</span><span class="sxs-lookup"><span data-stu-id="798b9-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="798b9-168">MsgStoreDlg</span><span class="sxs-lookup"><span data-stu-id="798b9-168">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="798b9-169">CMsgStoreDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="798b9-169">CMsgStoreDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="798b9-170">mfcmapi は、 **imapifolder::D eletefolder**メソッドを使用してフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="798b9-170">MFCMAPI uses the **IMAPIFolder::DeleteFolder** method to delete folders.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="798b9-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="798b9-171">See also</span></span>



[<span data-ttu-id="798b9-172">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="798b9-172">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="798b9-173">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="798b9-173">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

