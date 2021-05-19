---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d9c1e88b12baf50593212a3ae3c02907ce6617b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425660"
---
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="7f8ae-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="7f8ae-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="7f8ae-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f8ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f8ae-105">サブフォルダーをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-105">Copies or moves a subfolder.</span></span>
  
```cpp
HRESULT CopyFolder(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7f8ae-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7f8ae-106">Parameters</span></span>

 <span data-ttu-id="7f8ae-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7f8ae-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="7f8ae-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7f8ae-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7f8ae-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="7f8ae-110">[in]コピーまたは移動するサブフォルダーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="7f8ae-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7f8ae-111">_lpInterface_</span></span>
  
> <span data-ttu-id="7f8ae-112">[in]  _lpDestFolder_ パラメーターが指すフォルダーにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="7f8ae-113">NULL を渡すと、サービス プロバイダーは標準のフォルダー インターフェイス [IMAPIFolder : IMAPIContainer を返します](imapifolderimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="7f8ae-114">_lpInterface_ の有効な値には、IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、およびIID_IMAPIFolder。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="7f8ae-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="7f8ae-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="7f8ae-116">[in]コピーまたは移動されたサブフォルダーを受け取る開いているフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="7f8ae-117">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="7f8ae-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="7f8ae-118">[in]コピーまたは移動したフォルダーの新しい移動先の名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="7f8ae-119">_lpszNewFolderName_ が NULL に設定されている場合は、移動先フォルダーの名前にソース サブフォルダーの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="7f8ae-120">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7f8ae-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="7f8ae-121">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="7f8ae-122">_ulUIParam_ パラメーターは _、ulFlags_ パラメーター FOLDER_DIALOGフラグが設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="7f8ae-123">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="7f8ae-123">_lpProgress_</span></span>
  
> <span data-ttu-id="7f8ae-124">[in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="7f8ae-125">_lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="7f8ae-126">_lpProgress パラメーター_ は _、ulFlags_ で FOLDER_DIALOGフラグが設定されていない限り無視されます。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="7f8ae-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7f8ae-127">_ulFlags_</span></span>
  
> <span data-ttu-id="7f8ae-128">[in]コピーまたは移動操作を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="7f8ae-129">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-129">The following flags can be set:</span></span>
    
<span data-ttu-id="7f8ae-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="7f8ae-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="7f8ae-131">コピーするサブフォルダー内のすべてのサブフォルダーもコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="7f8ae-132">コピー COPY_SUBFOLDERS設定されていない場合は  _、lpEntryID_ で識別されるサブフォルダーだけがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="7f8ae-133">移動操作では、フラグCOPY_SUBFOLDERSに関係なく、既定の動作になります。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="7f8ae-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="7f8ae-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="7f8ae-135">進行状況インジケーターの表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="7f8ae-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="7f8ae-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="7f8ae-137">サブフォルダーはコピーの代わりに移動されます。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="7f8ae-138">このFOLDER_MOVE設定されていない場合、サブフォルダーがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="7f8ae-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="7f8ae-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="7f8ae-140">メッセージ ストア プロバイダーに、サポート オブジェクトの [IMAPISupport::D oCopyTo](imapisupport-docopyto.md)または [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md)メソッドを呼び出して **CopyFolder** を実装する場合 **、CopyFolder** は直ちに MAPI_E_DECLINE_COPY を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="7f8ae-141">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7f8ae-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7f8ae-142">移動先フォルダーの名前は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="7f8ae-143">このフラグMAPI_UNICODE設定されていない場合、フォルダー名は ANSI 形式です。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7f8ae-144">戻り値</span><span class="sxs-lookup"><span data-stu-id="7f8ae-144">Return value</span></span>

<span data-ttu-id="7f8ae-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f8ae-145">S_OK</span></span> 
  
> <span data-ttu-id="7f8ae-146">指定したフォルダーが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="7f8ae-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7f8ae-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7f8ae-148">MAPI_UNICODE フラグが設定され、メッセージ ストア プロバイダーが Unicode をサポートしていないか、または MAPI_UNICODEが設定されていないと、メッセージ ストア プロバイダーは Unicode のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="7f8ae-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="7f8ae-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="7f8ae-150">移動またはコピーされるフォルダーの名前は、移動先フォルダー内のサブフォルダーの名前と同じです。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="7f8ae-151">メッセージ ストア プロバイダーには、一意のフォルダー名が必要です。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="7f8ae-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="7f8ae-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="7f8ae-153">プロバイダーは、サポート オブジェクト メソッドを呼び出してこのメソッドを実装し、呼び出し元が MAPI_DECLINE_OK渡しました。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="7f8ae-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="7f8ae-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="7f8ae-155">ソース フォルダーには、直接または間接的に移動先フォルダーが含まれる。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="7f8ae-156">この条件が検出される前に重要な作業が実行された可能性があります。そのため、ソース フォルダーと移動先フォルダーが部分的に変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="7f8ae-157">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="7f8ae-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="7f8ae-158">呼び出しは成功しましたが、すべてのエントリが正常にコピーされたという訳ではありません。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="7f8ae-159">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7f8ae-160">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7f8ae-161">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f8ae-162">注釈</span><span class="sxs-lookup"><span data-stu-id="7f8ae-162">Remarks</span></span>

<span data-ttu-id="7f8ae-163">**IMAPIFolder::CopyFolder** メソッドは、サブフォルダーをある場所から別の場所にコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="7f8ae-164">コピーまたは移動するサブフォルダーは、サブフォルダーとして移動先フォルダーに追加されます。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7f8ae-165">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="7f8ae-165">Notes to implementers</span></span>

<span data-ttu-id="7f8ae-166">COPY_SUBFOLDERS フラグを設定することで示されている、コピーまたは移動操作に複数のフォルダーが含まれる場合は、フォルダーごとに可能な限り完全に操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="7f8ae-167">移動またはコピーするフォルダーの 1 つが存在しない場合や、既に他の場所に移動またはコピーされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="7f8ae-168">メモリの使い切れ、ディスク領域の使い切れ、メッセージ ストアの破損など、制御できないエラーが発生しない限り、操作を途中で停止しません。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="7f8ae-169">コピーされたメッセージ内のすべてのメッセージ エントリ識別子を保持してみてください。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="7f8ae-170">また、エントリ識別子を保持する必要がありますが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7f8ae-171">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7f8ae-171">Notes to callers</span></span>

<span data-ttu-id="7f8ae-172">これらの戻り値は、次の条件下で期待してください。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="7f8ae-173">**Condition**</span><span class="sxs-lookup"><span data-stu-id="7f8ae-173">**Condition**</span></span>|<span data-ttu-id="7f8ae-174">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="7f8ae-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7f8ae-175">**CopyFolder は** 、すべてのメッセージとサブフォルダーを正常にコピーまたは移動しました。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="7f8ae-176">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f8ae-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="7f8ae-177">**CopyFolder は** 、すべてのメッセージとサブフォルダーを正常にコピーまたは移動できなかった。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="7f8ae-178">MAPI_W_PARTIAL_COMPLETIONまたはMAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7f8ae-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="7f8ae-179">**CopyFolder** を完了できません。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="7f8ae-180">エラー以外のエラー MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7f8ae-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="7f8ae-181">**CopyFolder を** 完了できない場合は、作業が完了していないと想定しません。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="7f8ae-182">**エラーが発生する前に、CopyFolder** で 1 つ以上のメッセージとサブフォルダーをコピーまたは移動できた可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="7f8ae-183">存在しないフォルダーのエントリ識別子が  _lpEntryID_ で渡された場合 **、CopyFolder** はメッセージ ストアの実装に応じて MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="7f8ae-184">メッセージ ストア プロバイダーによっては、元のメッセージのエントリ識別子がコピーされたメッセージに保持される場合と保存されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="7f8ae-185">可能な限りエントリ識別子を保持する必要がありますが、要件ではありません。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="7f8ae-186">通常、次のシナリオに依存できます。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="7f8ae-187">2 つの異なる種類のメッセージ ストア間でフォルダーを移動すると、エントリ識別子が変更される保証があります。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="7f8ae-188">同じ種類の 2 つのメッセージ ストア間でフォルダーを移動すると、エントリ識別子はほとんど常に変更されます。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="7f8ae-189">フォルダーを同じメッセージ ストア内の別の場所に移動すると、メッセージ ストア プロバイダーによっては、エントリ識別子が変更される場合と変更されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="7f8ae-190">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="7f8ae-190">MFCMAPI reference</span></span>

<span data-ttu-id="7f8ae-191">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7f8ae-192">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="7f8ae-192">**File**</span></span>|<span data-ttu-id="7f8ae-193">**関数**</span><span class="sxs-lookup"><span data-stu-id="7f8ae-193">**Function**</span></span>|<span data-ttu-id="7f8ae-194">**コメント**</span><span class="sxs-lookup"><span data-stu-id="7f8ae-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7f8ae-195">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="7f8ae-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="7f8ae-196">CMsgStoreDlg::OnPasteFolder</span><span class="sxs-lookup"><span data-stu-id="7f8ae-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="7f8ae-197">MFCMAPI は **IMAPIFolder::CopyFolder** メソッドを使用して、フォルダーをある場所から別の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="7f8ae-198">MFCMAPI は、コピー操作中にソース フォルダーを記憶し、貼り付け操作中に実際にコピーを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f8ae-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7f8ae-199">関連項目</span><span class="sxs-lookup"><span data-stu-id="7f8ae-199">See also</span></span>



[<span data-ttu-id="7f8ae-200">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="7f8ae-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="7f8ae-201">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="7f8ae-201">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

