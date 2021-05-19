---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420886"
---
# <a name="imapisupportcopyfolder"></a><span data-ttu-id="837bb-103">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="837bb-103">IMAPISupport::CopyFolder</span></span>

  
  
<span data-ttu-id="837bb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="837bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="837bb-105">現在の親フォルダーから別の親フォルダーにフォルダーをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="837bb-105">Copies or moves a folder from its current parent folder to another parent folder.</span></span>
  
```cpp
HRESULT CopyFolder(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
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

## <a name="parameters"></a><span data-ttu-id="837bb-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="837bb-106">Parameters</span></span>

 <span data-ttu-id="837bb-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="837bb-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="837bb-108">[in]コピーまたは移動するフォルダーの親フォルダーにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="837bb-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the parent folder of the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="837bb-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="837bb-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="837bb-110">[in]コピーまたは移動するフォルダーの親フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="837bb-110">[in] A pointer to the parent folder of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="837bb-111">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="837bb-111">_cbEntryID_</span></span>
  
> <span data-ttu-id="837bb-112">[in]  _lpEntryID_ が指すエントリ識別子のバイト 数です。</span><span class="sxs-lookup"><span data-stu-id="837bb-112">[in] The byte count in the entry identifier pointed to by  _lpEntryID_.</span></span>
    
 <span data-ttu-id="837bb-113">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="837bb-113">_lpEntryID_</span></span>
  
> <span data-ttu-id="837bb-114">[in]コピーまたは移動するフォルダーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="837bb-114">[in] A pointer to the entry identifier of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="837bb-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="837bb-115">_lpInterface_</span></span>
  
> <span data-ttu-id="837bb-116">[in]予約済み。NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="837bb-116">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="837bb-117">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="837bb-117">_lpDestFolder_</span></span>
  
> <span data-ttu-id="837bb-118">[in]コピーまたは移動するフォルダーを受信するフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="837bb-118">[in] A pointer to the folder that is to receive the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="837bb-119">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="837bb-119">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="837bb-120">[in]コピーまたは移動されたフォルダーの名前へのポインター。それ以外の場合は、コピーまたは移動されたフォルダーがソース フォルダー  _(lpEntryID_ によって指されるフォルダー) と同じ名前を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="837bb-120">[in] A pointer to the name of the copied or moved folder; otherwise, NULL, which indicates that the copied or moved folder should have the same name as the source folder (the folder pointed to by  _lpEntryID_).</span></span>
    
 <span data-ttu-id="837bb-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="837bb-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="837bb-122">[in]進行状況インジケーター ダイアログ ボックスと関連するウィンドウのウィンドウのハンドル。</span><span class="sxs-lookup"><span data-stu-id="837bb-122">[in] A handle of the window for the progress indicator dialog box and related windows.</span></span> <span data-ttu-id="837bb-123">_ulUIParam_ パラメーターは _、ulFlags_ パラメーター FOLDER_DIALOGフラグが設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="837bb-123">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="837bb-124">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="837bb-124">_lpProgress_</span></span>
  
> <span data-ttu-id="837bb-125">[in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="837bb-125">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="837bb-126">_lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="837bb-126">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="837bb-127">_lpProgress パラメーター_ は _、ulFlags_ で FOLDER_DIALOGフラグが設定されていない限り無視されます。</span><span class="sxs-lookup"><span data-stu-id="837bb-127">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="837bb-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="837bb-128">_ulFlags_</span></span>
  
> <span data-ttu-id="837bb-129">[in]コピーまたは移動操作の実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="837bb-129">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="837bb-130">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="837bb-130">The following flags can be set:</span></span>
    
<span data-ttu-id="837bb-131">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="837bb-131">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="837bb-132">フォルダーのすべてのサブフォルダーをコピーまたは移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="837bb-132">All of the folder's subfolders should be copied or moved.</span></span> <span data-ttu-id="837bb-133">コピー COPY_SUBFOLDERS設定されていない場合は  _、lpEntryID_ で識別されるフォルダーだけがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="837bb-133">When COPY_SUBFOLDERS is not set for a copy operation, only the folder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="837bb-134">移動操作では、フラグCOPY_SUBFOLDERSに関係なく、既定の動作になります。</span><span class="sxs-lookup"><span data-stu-id="837bb-134">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="837bb-135">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="837bb-135">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="837bb-136">進行状況インジケーターの表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="837bb-136">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="837bb-137">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="837bb-137">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="837bb-138">フォルダーはコピーの代わりに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="837bb-138">The folder should be moved instead of copied.</span></span> <span data-ttu-id="837bb-139">このFOLDER_MOVE設定されていない場合は、フォルダーがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="837bb-139">If FOLDER_MOVE is not set, the folder is copied.</span></span>
    
<span data-ttu-id="837bb-140">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="837bb-140">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="837bb-141">フォルダーの名前は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="837bb-141">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="837bb-142">このフラグMAPI_UNICODE設定されていない場合、フォルダーの名前は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="837bb-142">If the MAPI_UNICODE flag is not set, the name of the folder is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="837bb-143">戻り値</span><span class="sxs-lookup"><span data-stu-id="837bb-143">Return value</span></span>

<span data-ttu-id="837bb-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="837bb-144">S_OK</span></span> 
  
> <span data-ttu-id="837bb-145">フォルダーが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="837bb-145">The folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="837bb-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="837bb-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="837bb-147">移動またはコピーされるフォルダーの名前は、移動先フォルダー内のサブフォルダーの名前と同じです。</span><span class="sxs-lookup"><span data-stu-id="837bb-147">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="837bb-148">メッセージ ストア プロバイダーでは、フォルダー名が一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="837bb-148">The message store provider requires that folder names be unique.</span></span> <span data-ttu-id="837bb-149">操作は完了せずに停止します。</span><span class="sxs-lookup"><span data-stu-id="837bb-149">The operation stops without completing.</span></span>
    
<span data-ttu-id="837bb-150">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="837bb-150">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="837bb-151">呼び出しは成功しましたが、すべてのエントリが正常にコピーされたという訳ではありません。</span><span class="sxs-lookup"><span data-stu-id="837bb-151">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="837bb-152">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="837bb-152">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="837bb-153">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="837bb-153">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="837bb-154">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="837bb-154">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="837bb-155">注釈</span><span class="sxs-lookup"><span data-stu-id="837bb-155">Remarks</span></span>

<span data-ttu-id="837bb-156">**IMAPISupport::CopyFolder** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="837bb-156">The **IMAPISupport::CopyFolder** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="837bb-157">メッセージ ストア プロバイダーは [、IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)の実装で **IMAPISupport::CopyFolder** を呼び出して、1 つのフォルダーを 1 つの親フォルダーから別の親フォルダーにコピーまたは移動できます。</span><span class="sxs-lookup"><span data-stu-id="837bb-157">Message store providers can call **IMAPISupport::CopyFolder** in their implementation of [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) to copy or move a single folder from one parent folder to another.</span></span> 
  
 <span data-ttu-id="837bb-158">**IMAPISupport::CopyFolder は** 、コピーまたは移動されたフォルダーを移動先フォルダーのサブフォルダーとして追加します。</span><span class="sxs-lookup"><span data-stu-id="837bb-158">**IMAPISupport::CopyFolder** adds the copied or moved folder as a subfolder of the destination folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="837bb-159">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="837bb-159">Notes to callers</span></span>

 <span data-ttu-id="837bb-160">**IMAPISupport::CopyFolder** を使用すると、フォルダーの名前の変更と移動、および影響を受けるフォルダーのサブフォルダーのコピーまたは移動を同時に実行できます。</span><span class="sxs-lookup"><span data-stu-id="837bb-160">**IMAPISupport::CopyFolder** allows simultaneous renaming and moving of folders and the copying or moving of subfolders of the affected folder.</span></span> <span data-ttu-id="837bb-161">コピーまたは移動したフォルダーに入れ子になったすべてのサブフォルダーをコピーまたは移動するには  _、ulFlags_ の COPY_SUBFOLDERS フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="837bb-161">To copy or move all subfolders nested in the copied or moved folder, pass the COPY_SUBFOLDERS flag in  _ulFlags_.</span></span> 
  
<span data-ttu-id="837bb-162">次の条件の下で、次の戻り値を期待します。</span><span class="sxs-lookup"><span data-stu-id="837bb-162">Expect the following return values under the following conditions:</span></span>
  
|<span data-ttu-id="837bb-163">**Condition**</span><span class="sxs-lookup"><span data-stu-id="837bb-163">**Condition**</span></span>|<span data-ttu-id="837bb-164">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="837bb-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="837bb-165">**CopyFolder は** 、該当する場合は、フォルダーとそのすべてのサブフォルダーを正常にコピーまたは移動しました。</span><span class="sxs-lookup"><span data-stu-id="837bb-165">**CopyFolder** successfully copied or moved the folder and all its subfolders, if applicable.</span></span>  <br/> |<span data-ttu-id="837bb-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="837bb-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="837bb-167">**CopyFolder** は、すべてのフォルダーを正常にコピーまたは移動できなかった。</span><span class="sxs-lookup"><span data-stu-id="837bb-167">**CopyFolder** was unable to successfully copy or move all of the folders.</span></span>  <br/> |<span data-ttu-id="837bb-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="837bb-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="837bb-169">**CopyFolder** を完了できません。</span><span class="sxs-lookup"><span data-stu-id="837bb-169">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="837bb-170">エラー値</span><span class="sxs-lookup"><span data-stu-id="837bb-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="837bb-171">**CopyFolder がエラー** 値を返す場合は、作業が完了していないという前提で続行しません。</span><span class="sxs-lookup"><span data-stu-id="837bb-171">If **CopyFolder** returns an error value, do not proceed on the assumption that no work was done.</span></span> <span data-ttu-id="837bb-172">**CopyFolder** でエラーが発生する前に、1 つ以上のフォルダーがコピーまたは移動されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="837bb-172">One or more folders could have been copied or moved before **CopyFolder** experienced the failure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="837bb-173">関連項目</span><span class="sxs-lookup"><span data-stu-id="837bb-173">See also</span></span>



[<span data-ttu-id="837bb-174">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="837bb-174">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

