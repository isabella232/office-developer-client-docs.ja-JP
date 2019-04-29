---
title: imapisupportcopyfolder
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
# <a name="imapisupportcopyfolder"></a><span data-ttu-id="a0627-103">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="a0627-103">IMAPISupport::CopyFolder</span></span>

  
  
<span data-ttu-id="a0627-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0627-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0627-105">フォルダーを現在の親フォルダーから別の親フォルダーにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="a0627-105">Copies or moves a folder from its current parent folder to another parent folder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="a0627-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a0627-106">Parameters</span></span>

 <span data-ttu-id="a0627-107">_lpsrcinterface_</span><span class="sxs-lookup"><span data-stu-id="a0627-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="a0627-108">順番コピーまたは移動するフォルダーの親フォルダーにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0627-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the parent folder of the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="a0627-109">_lpsrcfolder_</span><span class="sxs-lookup"><span data-stu-id="a0627-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="a0627-110">順番コピーまたは移動するフォルダーの親フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0627-110">[in] A pointer to the parent folder of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="a0627-111">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a0627-111">_cbEntryID_</span></span>
  
> <span data-ttu-id="a0627-112">順番エントリ識別子のバイト数が_lな tryid_で示されます。</span><span class="sxs-lookup"><span data-stu-id="a0627-112">[in] The byte count in the entry identifier pointed to by  _lpEntryID_.</span></span>
    
 <span data-ttu-id="a0627-113">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="a0627-113">_lpEntryID_</span></span>
  
> <span data-ttu-id="a0627-114">順番コピーまたは移動するフォルダーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0627-114">[in] A pointer to the entry identifier of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="a0627-115">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="a0627-115">_lpInterface_</span></span>
  
> <span data-ttu-id="a0627-116">順番予約語NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0627-116">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="a0627-117">_lpdestfolder_</span><span class="sxs-lookup"><span data-stu-id="a0627-117">_lpDestFolder_</span></span>
  
> <span data-ttu-id="a0627-118">順番コピーまたは移動するフォルダーを受け取るフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0627-118">[in] A pointer to the folder that is to receive the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="a0627-119">_lpsznewfoldername_</span><span class="sxs-lookup"><span data-stu-id="a0627-119">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="a0627-120">順番コピーまたは移動したフォルダーの名前へのポインター。それ以外の場合は、コピーまたは移動されたフォルダーの名前がソースフォルダーと同じであることを示します ( _lな tryid_で示されるフォルダー)。</span><span class="sxs-lookup"><span data-stu-id="a0627-120">[in] A pointer to the name of the copied or moved folder; otherwise, NULL, which indicates that the copied or moved folder should have the same name as the source folder (the folder pointed to by  _lpEntryID_).</span></span>
    
 <span data-ttu-id="a0627-121">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="a0627-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="a0627-122">順番[進行状況インジケーター] ダイアログボックスと関連するウィンドウのウィンドウのハンドル。</span><span class="sxs-lookup"><span data-stu-id="a0627-122">[in] A handle of the window for the progress indicator dialog box and related windows.</span></span> <span data-ttu-id="a0627-123">_uluiparam_パラメーターは、 _ulflags_パラメーターで FOLDER_DIALOG フラグが設定されていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="a0627-123">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a0627-124">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="a0627-124">_lpProgress_</span></span>
  
> <span data-ttu-id="a0627-125">順番進行状況インジケーターを表示する progress オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0627-125">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="a0627-126">_lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="a0627-126">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="a0627-127">FOLDER_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a0627-127">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="a0627-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0627-128">_ulFlags_</span></span>
  
> <span data-ttu-id="a0627-129">順番コピー操作または移動操作の実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a0627-129">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="a0627-130">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0627-130">The following flags can be set:</span></span>
    
<span data-ttu-id="a0627-131">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="a0627-131">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="a0627-132">すべてのフォルダーのサブフォルダーをコピーまたは移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0627-132">All of the folder's subfolders should be copied or moved.</span></span> <span data-ttu-id="a0627-133">コピー操作で COPY_SUBFOLDERS が設定されていない場合は、 _l tryid_で識別されるフォルダーのみがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a0627-133">When COPY_SUBFOLDERS is not set for a copy operation, only the folder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="a0627-134">移動操作では、フラグが設定されているかどうかに関係なく、COPY_SUBFOLDERS の動作が既定値になります。</span><span class="sxs-lookup"><span data-stu-id="a0627-134">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="a0627-135">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a0627-135">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="a0627-136">進行状況インジケーターの表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="a0627-136">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="a0627-137">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="a0627-137">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="a0627-138">フォルダーはコピーではなく移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0627-138">The folder should be moved instead of copied.</span></span> <span data-ttu-id="a0627-139">FOLDER_MOVE が設定されていない場合は、フォルダーがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a0627-139">If FOLDER_MOVE is not set, the folder is copied.</span></span>
    
<span data-ttu-id="a0627-140">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a0627-140">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a0627-141">フォルダーの名前は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="a0627-141">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="a0627-142">MAPI_UNICODE フラグが設定されていない場合、フォルダーの名前は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="a0627-142">If the MAPI_UNICODE flag is not set, the name of the folder is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a0627-143">戻り値</span><span class="sxs-lookup"><span data-stu-id="a0627-143">Return value</span></span>

<span data-ttu-id="a0627-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0627-144">S_OK</span></span> 
  
> <span data-ttu-id="a0627-145">フォルダーが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="a0627-145">The folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="a0627-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="a0627-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="a0627-147">移動またはコピーするフォルダーの名前が、移動先フォルダーのサブフォルダーの名前と同じです。</span><span class="sxs-lookup"><span data-stu-id="a0627-147">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="a0627-148">メッセージストアプロバイダーでは、フォルダー名が一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0627-148">The message store provider requires that folder names be unique.</span></span> <span data-ttu-id="a0627-149">操作は完了せずに停止します。</span><span class="sxs-lookup"><span data-stu-id="a0627-149">The operation stops without completing.</span></span>
    
<span data-ttu-id="a0627-150">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="a0627-150">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="a0627-151">呼び出しは成功しましたが、すべてのエントリが正常にコピーされませんでした。</span><span class="sxs-lookup"><span data-stu-id="a0627-151">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="a0627-152">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="a0627-152">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a0627-153">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="a0627-153">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a0627-154">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0627-154">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0627-155">注釈</span><span class="sxs-lookup"><span data-stu-id="a0627-155">Remarks</span></span>

<span data-ttu-id="a0627-156">**imapisupport:: copyfolder**メソッドは、メッセージストアプロバイダーサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="a0627-156">The **IMAPISupport::CopyFolder** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="a0627-157">メッセージストアプロバイダーは、 [imapisupport:](imapifolder-copyfolder.md) : copyfolder の実装で**imapisupport:: copyfolder**を呼び出して、1つの親フォルダーから別のフォルダーに1つのフォルダーをコピーまたは移動することができます。</span><span class="sxs-lookup"><span data-stu-id="a0627-157">Message store providers can call **IMAPISupport::CopyFolder** in their implementation of [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) to copy or move a single folder from one parent folder to another.</span></span> 
  
 <span data-ttu-id="a0627-158">**imapisupport:: copyfolder**移動先フォルダーのサブフォルダーとして、コピーまたは移動したフォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="a0627-158">**IMAPISupport::CopyFolder** adds the copied or moved folder as a subfolder of the destination folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a0627-159">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a0627-159">Notes to callers</span></span>

 <span data-ttu-id="a0627-160">**imapisupport:: copyfolder**を使用すると、フォルダーの名前変更と移動、および影響を受けたフォルダーのサブフォルダーのコピーまたは移動を同時に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a0627-160">**IMAPISupport::CopyFolder** allows simultaneous renaming and moving of folders and the copying or moving of subfolders of the affected folder.</span></span> <span data-ttu-id="a0627-161">コピーまたは移動したフォルダーでネストされているすべてのサブフォルダーをコピーまたは移動するには、COPY_SUBFOLDERS フラグを_ulflags_に渡します。</span><span class="sxs-lookup"><span data-stu-id="a0627-161">To copy or move all subfolders nested in the copied or moved folder, pass the COPY_SUBFOLDERS flag in  _ulFlags_.</span></span> 
  
<span data-ttu-id="a0627-162">次の条件下では、次の戻り値が予想されます。</span><span class="sxs-lookup"><span data-stu-id="a0627-162">Expect the following return values under the following conditions:</span></span>
  
|<span data-ttu-id="a0627-163">**Condition**</span><span class="sxs-lookup"><span data-stu-id="a0627-163">**Condition**</span></span>|<span data-ttu-id="a0627-164">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="a0627-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0627-165">\*\*\*\* 必要に応じて、フォルダーとそのすべてのサブフォルダーがコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="a0627-165">**CopyFolder** successfully copied or moved the folder and all its subfolders, if applicable.</span></span>  <br/> |<span data-ttu-id="a0627-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0627-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="a0627-167">**copyfolder**は、すべてのフォルダーを正常にコピーまたは移動できませんでした。</span><span class="sxs-lookup"><span data-stu-id="a0627-167">**CopyFolder** was unable to successfully copy or move all of the folders.</span></span>  <br/> |<span data-ttu-id="a0627-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="a0627-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="a0627-169">**copyfolder**を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="a0627-169">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="a0627-170">任意のエラー値</span><span class="sxs-lookup"><span data-stu-id="a0627-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="a0627-171">**copyfolder**がエラー値を返した場合は、処理が行われていないという前提で続行しないでください。</span><span class="sxs-lookup"><span data-stu-id="a0627-171">If **CopyFolder** returns an error value, do not proceed on the assumption that no work was done.</span></span> <span data-ttu-id="a0627-172">**copyfolder**でエラーが発生する前に、1つ以上のフォルダーがコピーまたは移動された可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0627-172">One or more folders could have been copied or moved before **CopyFolder** experienced the failure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0627-173">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0627-173">See also</span></span>



[<span data-ttu-id="a0627-174">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0627-174">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

