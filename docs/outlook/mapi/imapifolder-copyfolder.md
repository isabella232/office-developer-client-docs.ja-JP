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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 134a492dbc86dd0ce6b3795d5ae40b334c14d468
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585151"
---
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="2be86-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="2be86-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="2be86-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2be86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2be86-105">サブフォルダーを移動またはコピーします。</span><span class="sxs-lookup"><span data-stu-id="2be86-105">Copies or moves a subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="2be86-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2be86-106">Parameters</span></span>

 <span data-ttu-id="2be86-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2be86-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="2be86-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="2be86-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2be86-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="2be86-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="2be86-110">[in]サブフォルダーをコピーまたは移動するには、エントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2be86-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="2be86-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="2be86-111">_lpInterface_</span></span>
  
> <span data-ttu-id="2be86-112">[in]_LpDestFolder_パラメーターが指すフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2be86-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="2be86-113">フォルダーの標準的なインターフェイスを取得するサービス プロバイダーは、NULL を渡す[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="2be86-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="2be86-114">に対する、IID_IMAPIProp、IID_IMAPIContainer、IID_IMAPIFolder、 _lpInterface_の有効な値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2be86-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="2be86-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="2be86-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="2be86-116">[in]開いているフォルダーにコピーまたは移動したサブフォルダーが表示されるへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2be86-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="2be86-117">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="2be86-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="2be86-118">[in]その新しい場所にコピーまたは移動したフォルダーの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2be86-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="2be86-119">_LpszNewFolderName_は、NULL に設定されている場合、コピー先のフォルダーの名前の複製元のサブフォルダーの名前が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2be86-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="2be86-120">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2be86-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="2be86-121">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="2be86-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="2be86-122">_UlFlags_パラメーターに FOLDER_DIALOG フラグが設定されていない場合、 _ulUIParam_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2be86-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="2be86-123">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="2be86-123">_lpProgress_</span></span>
  
> <span data-ttu-id="2be86-124">[in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2be86-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="2be86-125">_LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="2be86-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="2be86-126">_UlFlags_に FOLDER_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2be86-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="2be86-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2be86-127">_ulFlags_</span></span>
  
> <span data-ttu-id="2be86-128">[in]コピーまたは移動操作を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="2be86-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="2be86-129">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="2be86-129">The following flags can be set:</span></span>
    
<span data-ttu-id="2be86-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="2be86-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="2be86-131">すべてのサブフォルダーにコピーされるサブフォルダーにもコピーしてください。</span><span class="sxs-lookup"><span data-stu-id="2be86-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="2be86-132">コピー操作の COPY_SUBFOLDERS が設定されていない、 _lpEntryID_で識別されるサブフォルダーのみがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="2be86-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="2be86-133">移動操作で、COPY_SUBFOLDERS の動作は既定のフラグが設定されているかどうかに関係なくです。</span><span class="sxs-lookup"><span data-stu-id="2be86-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="2be86-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2be86-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="2be86-135">進行状況インジケーターの表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="2be86-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="2be86-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="2be86-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="2be86-137">代わりに移動するのには、サブフォルダーをコピーします。</span><span class="sxs-lookup"><span data-stu-id="2be86-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="2be86-138">FOLDER_MOVE が設定されていない場合は、サブフォルダーがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="2be86-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="2be86-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="2be86-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="2be86-140">**CopyFolder**メソッドのサポート オブジェクトの[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)または[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)メソッドを呼び出すことによって実装されている場合は、 **CopyFolder**する必要があります代わりにすぐに返すこと MAPI_E_、メッセージ ストア プロバイダーの通知します。DECLINE_COPY。</span><span class="sxs-lookup"><span data-stu-id="2be86-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="2be86-141">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2be86-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2be86-142">Unicode 形式では、コピー先のフォルダーの名前です。</span><span class="sxs-lookup"><span data-stu-id="2be86-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="2be86-143">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のフォルダー名です。</span><span class="sxs-lookup"><span data-stu-id="2be86-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2be86-144">�߂�l</span><span class="sxs-lookup"><span data-stu-id="2be86-144">Return value</span></span>

<span data-ttu-id="2be86-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="2be86-145">S_OK</span></span> 
  
> <span data-ttu-id="2be86-146">指定されたフォルダーは正常にコピーまたは移動されています。</span><span class="sxs-lookup"><span data-stu-id="2be86-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="2be86-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2be86-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2be86-148">か、MAPI_UNICODE フラグが設定されたメッセージ ストア プロバイダーは、Unicode をサポートしていないまたは MAPI_UNICODE が設定されていないとメッセージ ストア プロバイダーは、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2be86-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="2be86-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="2be86-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="2be86-150">移動またはコピーされているフォルダーの名前は、コピー先のフォルダーのサブフォルダーの名前と同じです。</span><span class="sxs-lookup"><span data-stu-id="2be86-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="2be86-151">メッセージ ストア プロバイダーには、一意のフォルダー名が必要です。</span><span class="sxs-lookup"><span data-stu-id="2be86-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="2be86-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="2be86-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="2be86-153">プロバイダーのサポートのオブジェクトのメソッドを呼び出すことによってこのメソッドを実装して、呼び出し元に MAPI_DECLINE_OK フラグが渡されます。</span><span class="sxs-lookup"><span data-stu-id="2be86-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="2be86-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="2be86-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="2be86-155">ソースフォルダーには直接的または間接的にコピー先のフォルダーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2be86-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="2be86-156">作業時間の大幅な可能性がありますが完了前に、この条件が検出された、元とコピー先のフォルダーを部分的に変更された可能性がありますので。</span><span class="sxs-lookup"><span data-stu-id="2be86-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="2be86-157">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="2be86-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="2be86-158">呼び出しが成功したが、すべてのエントリが正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="2be86-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="2be86-159">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2be86-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="2be86-160">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="2be86-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="2be86-161">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2be86-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2be86-162">注釈</span><span class="sxs-lookup"><span data-stu-id="2be86-162">Remarks</span></span>

<span data-ttu-id="2be86-163">**IMAPIFolder::CopyFolder**メソッドは、コピーまたはサブフォルダーを別の場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="2be86-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="2be86-164">サブフォルダーのコピーや移動は、サブフォルダーとして、コピー先のフォルダーに追加されます。</span><span class="sxs-lookup"><span data-stu-id="2be86-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2be86-165">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="2be86-165">Notes to implementers</span></span>

<span data-ttu-id="2be86-166">コピーまたは移動操作には、COPY_SUBFOLDERS フラグを設定することによって示されているように、複数のフォルダーが含まれている場合、可能な限り完全にフォルダーごとに操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="2be86-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="2be86-167">移動またはコピーするフォルダーのいずれかの場合があります存在しないまたは既に移動または別の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="2be86-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="2be86-168">メモリが不足している、ディスク領域、またはメッセージ ・ ストア内の破損が不足しているなど、ユーザーが制御できない障害が発生した場合を除きは、処理の途中で操作を停止しません。</span><span class="sxs-lookup"><span data-stu-id="2be86-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="2be86-169">コピーしたメッセージですべてのメッセージ エントリの識別子を保持しようとしてください。</span><span class="sxs-lookup"><span data-stu-id="2be86-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="2be86-170">エントリの識別子を保持するためにも実行してくださいする必要がありますが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="2be86-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2be86-171">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2be86-171">Notes to callers</span></span>

<span data-ttu-id="2be86-172">次の条件下で、これらの戻り値を期待してください。</span><span class="sxs-lookup"><span data-stu-id="2be86-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="2be86-173">**条件**</span><span class="sxs-lookup"><span data-stu-id="2be86-173">**Condition**</span></span>|<span data-ttu-id="2be86-174">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="2be86-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2be86-175">**CopyFolder**が正常にコピーまたは、すべてのメッセージとサブフォルダーを移動します。</span><span class="sxs-lookup"><span data-stu-id="2be86-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="2be86-176">S_OK</span><span class="sxs-lookup"><span data-stu-id="2be86-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="2be86-177">**CopyFolder**は、正常にコピーまたはすべてのメッセージとサブフォルダーに移動できませんでした。</span><span class="sxs-lookup"><span data-stu-id="2be86-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="2be86-178">MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2be86-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="2be86-179">**CopyFolder**は完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="2be86-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="2be86-180">MAPI_E_NOT_FOUND を除くエラー値</span><span class="sxs-lookup"><span data-stu-id="2be86-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="2be86-181">**CopyFolder**が完了することではない場合と仮定しないでその作業は実行されませんでした。</span><span class="sxs-lookup"><span data-stu-id="2be86-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="2be86-182">**CopyFolder**をコピーまたはエラーが発生する前に 1 つまたは複数のメッセージとサブフォルダーを移動することがされている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2be86-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="2be86-183">_LpEntryID_で存在しないフォルダーのエントリ id が渡された場合に、 **CopyFolder**は、メッセージ ストアの実装によって MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="2be86-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="2be86-184">によって、メッセージ ストア プロバイダーでは、元のメッセージのエントリ id は、コピーされたメッセージには保持されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="2be86-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="2be86-185">可能な限り、エントリの識別子を保持する必要がありますが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="2be86-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="2be86-186">一般に次のシナリオに依存します。</span><span class="sxs-lookup"><span data-stu-id="2be86-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="2be86-187">2 種類のメッセージ ・ ストア間でフォルダーを移動するときを変更するエントリの識別子が保証されます。</span><span class="sxs-lookup"><span data-stu-id="2be86-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="2be86-188">同じ種類の 2 つのメッセージ ストア間でフォルダーを移動するときにほとんどのエントリ id を変更します。</span><span class="sxs-lookup"><span data-stu-id="2be86-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="2be86-189">同じメッセージ ・ ストア内の別の場所にフォルダーを移動すると、エントリの識別子または可能性がありますしない変更、メッセージによって、プロバイダーを格納します。</span><span class="sxs-lookup"><span data-stu-id="2be86-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="2be86-190">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="2be86-190">MFCMAPI reference</span></span>

<span data-ttu-id="2be86-191">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="2be86-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2be86-192">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="2be86-192">**File**</span></span>|<span data-ttu-id="2be86-193">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="2be86-193">**Function**</span></span>|<span data-ttu-id="2be86-194">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="2be86-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2be86-195">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2be86-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="2be86-196">CMsgStoreDlg::OnPasteFolder</span><span class="sxs-lookup"><span data-stu-id="2be86-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="2be86-197">MFCMAPI では、1 つの場所からフォルダーをコピーするのにには、 **IMAPIFolder::CopyFolder**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2be86-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="2be86-198">MFCMAPI では、コピー操作中に元のフォルダーを記憶して、実際に貼り付けの操作中にコピーを実行します。</span><span class="sxs-lookup"><span data-stu-id="2be86-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2be86-199">関連項目</span><span class="sxs-lookup"><span data-stu-id="2be86-199">See also</span></span>



[<span data-ttu-id="2be86-200">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="2be86-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="2be86-201">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2be86-201">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

