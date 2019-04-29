---
title: imapifoldercopyfolder
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
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="9546a-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="9546a-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="9546a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9546a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9546a-105">サブフォルダーをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="9546a-105">Copies or moves a subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="9546a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9546a-106">Parameters</span></span>

 <span data-ttu-id="9546a-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="9546a-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="9546a-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="9546a-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="9546a-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="9546a-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="9546a-110">順番コピーまたは移動するサブフォルダーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9546a-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="9546a-111">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="9546a-111">_lpInterface_</span></span>
  
> <span data-ttu-id="9546a-112">順番_lpdestfolder_パラメーターが指すフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9546a-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="9546a-113">NULL を渡すと、サービスプロバイダーは標準のフォルダーインターフェイス、 [imapifolder: IMAPIContainer](imapifolderimapicontainer.md)を返します。</span><span class="sxs-lookup"><span data-stu-id="9546a-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="9546a-114">_lpinterface_の有効な値は、IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、および IID_IMAPIFolder です。</span><span class="sxs-lookup"><span data-stu-id="9546a-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="9546a-115">_lpdestfolder_</span><span class="sxs-lookup"><span data-stu-id="9546a-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="9546a-116">順番コピーまたは移動したサブフォルダーを受け取るための、開いているフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9546a-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="9546a-117">_lpsznewfoldername_</span><span class="sxs-lookup"><span data-stu-id="9546a-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="9546a-118">順番コピーまたは移動先のフォルダーの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9546a-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="9546a-119">_lpsznewfoldername_が NULL に設定されている場合、source サブフォルダーの名前が宛先フォルダーの名前として使用されます。</span><span class="sxs-lookup"><span data-stu-id="9546a-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="9546a-120">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="9546a-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="9546a-121">順番進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="9546a-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="9546a-122">_uluiparam_パラメーターは、 _ulflags_パラメーターの FOLDER_DIALOG フラグが設定されていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="9546a-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="9546a-123">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="9546a-123">_lpProgress_</span></span>
  
> <span data-ttu-id="9546a-124">順番進行状況インジケーターを表示する progress オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9546a-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="9546a-125">_lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="9546a-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="9546a-126">FOLDER_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="9546a-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="9546a-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9546a-127">_ulFlags_</span></span>
  
> <span data-ttu-id="9546a-128">順番コピー操作または移動操作を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="9546a-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="9546a-129">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9546a-129">The following flags can be set:</span></span>
    
<span data-ttu-id="9546a-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="9546a-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="9546a-131">コピーするサブフォルダー内のすべてのサブフォルダーもコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9546a-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="9546a-132">コピー操作で COPY_SUBFOLDERS が設定されていない場合は、 _l tryid_で識別されるサブフォルダーのみがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="9546a-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="9546a-133">移動操作では、フラグが設定されているかどうかに関係なく、COPY_SUBFOLDERS の動作が既定値になります。</span><span class="sxs-lookup"><span data-stu-id="9546a-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="9546a-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9546a-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="9546a-135">進行状況インジケーターの表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="9546a-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="9546a-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="9546a-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="9546a-137">サブフォルダーはコピーではなく移動されます。</span><span class="sxs-lookup"><span data-stu-id="9546a-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="9546a-138">FOLDER_MOVE が設定されていない場合は、サブフォルダーがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="9546a-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="9546a-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="9546a-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="9546a-140">サポートオブジェクトの imapisupport を呼び出して**copyfolder**を実装する場合に、メッセージストアプロバイダーに通知します[。:D ocopyto](imapisupport-docopyto.md)または[imapisupport::D ocopyprops](imapisupport-docopyprops.md)メソッド、 **copyfolder**はすぐに MAPI_E_ を返す必要があります。DECLINE_COPY。</span><span class="sxs-lookup"><span data-stu-id="9546a-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="9546a-141">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9546a-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9546a-142">宛先フォルダーの名前は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="9546a-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="9546a-143">MAPI_UNICODE フラグが設定されていない場合、フォルダー名は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="9546a-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9546a-144">戻り値</span><span class="sxs-lookup"><span data-stu-id="9546a-144">Return value</span></span>

<span data-ttu-id="9546a-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="9546a-145">S_OK</span></span> 
  
> <span data-ttu-id="9546a-146">指定したフォルダーが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="9546a-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="9546a-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9546a-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9546a-148">MAPI_UNICODE フラグが設定されており、メッセージストアプロバイダーが unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、メッセージストアプロバイダーが unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9546a-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="9546a-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="9546a-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="9546a-150">移動またはコピーするフォルダーの名前が、移動先フォルダーのサブフォルダーの名前と同じです。</span><span class="sxs-lookup"><span data-stu-id="9546a-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="9546a-151">メッセージストアプロバイダーには、一意のフォルダー名が必要です。</span><span class="sxs-lookup"><span data-stu-id="9546a-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="9546a-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="9546a-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="9546a-153">プロバイダーは、サポートオブジェクトのメソッドを呼び出すことによってこのメソッドを実装し、発信者が MAPI_DECLINE_OK フラグを渡しています。</span><span class="sxs-lookup"><span data-stu-id="9546a-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="9546a-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="9546a-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="9546a-155">ソースフォルダーが直接または間接的に、宛先フォルダーを含んでいる。</span><span class="sxs-lookup"><span data-stu-id="9546a-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="9546a-156">この条件が検出される前に、重要な作業が実行されている可能性があるため、ソースフォルダーと宛先フォルダーの一部が変更されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9546a-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="9546a-157">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="9546a-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="9546a-158">呼び出しは成功しましたが、すべてのエントリが正常にコピーされませんでした。</span><span class="sxs-lookup"><span data-stu-id="9546a-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="9546a-159">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="9546a-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="9546a-160">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="9546a-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="9546a-161">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9546a-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9546a-162">注釈</span><span class="sxs-lookup"><span data-stu-id="9546a-162">Remarks</span></span>

<span data-ttu-id="9546a-163">**imapifolder:: copyfolder**メソッドは、ある場所から別の場所にサブフォルダーをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="9546a-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="9546a-164">コピーまたは移動しているサブフォルダーは、サブフォルダーとして、宛先フォルダーに追加されます。</span><span class="sxs-lookup"><span data-stu-id="9546a-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9546a-165">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="9546a-165">Notes to implementers</span></span>

<span data-ttu-id="9546a-166">コピー操作または移動操作で、COPY_SUBFOLDERS フラグを設定することによって複数のフォルダーが含まれている場合は、その操作を各フォルダーで可能な限り完全に実行します。</span><span class="sxs-lookup"><span data-stu-id="9546a-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="9546a-167">移動またはコピーするフォルダーの1つが存在しない場合や、別の場所に移動またはコピーされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="9546a-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="9546a-168">メモリが不足している、ディスクの空き領域が不足している、メッセージストアが破損しているなど、操作を途中で停止しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="9546a-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="9546a-169">コピーしたメッセージのすべてのメッセージエントリ識別子を保持するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="9546a-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="9546a-170">また、エントリ識別子を保持する必要はありませんが、これは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="9546a-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9546a-171">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="9546a-171">Notes to callers</span></span>

<span data-ttu-id="9546a-172">これらの戻り値は、次の条件に当てはまることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="9546a-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="9546a-173">**Condition**</span><span class="sxs-lookup"><span data-stu-id="9546a-173">**Condition**</span></span>|<span data-ttu-id="9546a-174">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="9546a-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9546a-175">**copyfolder**は、メッセージとサブフォルダーごとに正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="9546a-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="9546a-176">S_OK</span><span class="sxs-lookup"><span data-stu-id="9546a-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="9546a-177">**copyfolder**は、すべてのメッセージとサブフォルダを正常にコピーまたは移動できませんでした。</span><span class="sxs-lookup"><span data-stu-id="9546a-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="9546a-178">MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9546a-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="9546a-179">**copyfolder**を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="9546a-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="9546a-180">MAPI_E_NOT_FOUND を除くすべてのエラー値</span><span class="sxs-lookup"><span data-stu-id="9546a-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="9546a-181">**copyfolder**を完了できない場合でも、作業が行われていないとは限りません。</span><span class="sxs-lookup"><span data-stu-id="9546a-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="9546a-182">エラーが発生する前に、 **copyfolder**が1つ以上のメッセージとサブフォルダーをコピーまたは移動できた可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9546a-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="9546a-183">存在しないフォルダーのエントリ識別子が_lMAPI_W_PARTIAL_COMPLETION tryid_で渡された場合、 **copyfolder**は、メッセージストアの実装に応じて、または MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="9546a-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="9546a-184">メッセージストアプロバイダーによっては、元のメッセージのエントリ識別子がコピーされたメッセージに保持されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="9546a-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="9546a-185">可能な限り、エントリ識別子は保持する必要がありますが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="9546a-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="9546a-186">通常は、次のシナリオに依存します。</span><span class="sxs-lookup"><span data-stu-id="9546a-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="9546a-187">2つの異なる種類のメッセージストア間でフォルダーを移動する場合、エントリ識別子の変更は保証されます。</span><span class="sxs-lookup"><span data-stu-id="9546a-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="9546a-188">同じ種類の2つのメッセージストア間でフォルダーを移動する場合、エントリ識別子はほぼ常に変更されます。</span><span class="sxs-lookup"><span data-stu-id="9546a-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="9546a-189">フォルダーを同じメッセージストア内の別の場所に移動すると、メッセージストアプロバイダーによっては、エントリ識別子が変更されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="9546a-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="9546a-190">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="9546a-190">MFCMAPI reference</span></span>

<span data-ttu-id="9546a-191">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9546a-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9546a-192">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="9546a-192">**File**</span></span>|<span data-ttu-id="9546a-193">**関数**</span><span class="sxs-lookup"><span data-stu-id="9546a-193">**Function**</span></span>|<span data-ttu-id="9546a-194">**コメント**</span><span class="sxs-lookup"><span data-stu-id="9546a-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9546a-195">MsgStoreDlg</span><span class="sxs-lookup"><span data-stu-id="9546a-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="9546a-196">CMsgStoreDlg:: OnPasteFolder</span><span class="sxs-lookup"><span data-stu-id="9546a-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="9546a-197">mfcmapi は、 **imapifolder:: copyfolder**メソッドを使用して、フォルダーをある場所から別の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="9546a-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="9546a-198">mfcmapi はコピー操作中にソースフォルダーを記憶し、貼り付け操作中にコピーを実際に実行します。</span><span class="sxs-lookup"><span data-stu-id="9546a-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9546a-199">関連項目</span><span class="sxs-lookup"><span data-stu-id="9546a-199">See also</span></span>



[<span data-ttu-id="9546a-200">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="9546a-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="9546a-201">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="9546a-201">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

