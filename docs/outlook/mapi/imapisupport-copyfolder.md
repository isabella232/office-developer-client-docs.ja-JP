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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0b079b311a68459a43b0a7659ddfbe94d96d7f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800721"
---
# <a name="imapisupportcopyfolder"></a><span data-ttu-id="50d41-103">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="50d41-103">IMAPISupport::CopyFolder</span></span>

  
  
<span data-ttu-id="50d41-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="50d41-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="50d41-105">現在の親フォルダーから別の親フォルダーにフォルダーを移動またはコピーします。</span><span class="sxs-lookup"><span data-stu-id="50d41-105">Copies or moves a folder from its current parent folder to another parent folder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="50d41-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50d41-106">Parameters</span></span>

 <span data-ttu-id="50d41-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="50d41-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="50d41-108">[in]コピーまたは移動するフォルダーの親フォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="50d41-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the parent folder of the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="50d41-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="50d41-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="50d41-110">[in]コピーまたは移動するフォルダーの親フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="50d41-110">[in] A pointer to the parent folder of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="50d41-111">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="50d41-111">_cbEntryID_</span></span>
  
> <span data-ttu-id="50d41-112">[in]_LpEntryID_で指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="50d41-112">[in] The byte count in the entry identifier pointed to by  _lpEntryID_.</span></span>
    
 <span data-ttu-id="50d41-113">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="50d41-113">_lpEntryID_</span></span>
  
> <span data-ttu-id="50d41-114">[in]コピーまたは移動するフォルダーのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="50d41-114">[in] A pointer to the entry identifier of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="50d41-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="50d41-115">_lpInterface_</span></span>
  
> <span data-ttu-id="50d41-116">[in]予約されています。NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="50d41-116">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="50d41-117">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="50d41-117">_lpDestFolder_</span></span>
  
> <span data-ttu-id="50d41-118">[in]コピーまたは移動するフォルダーを受信するフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="50d41-118">[in] A pointer to the folder that is to receive the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="50d41-119">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="50d41-119">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="50d41-120">[in]コピーまたは移動したフォルダーの名前へのポインターそれ以外の場合、NULL、コピーまたは移動したフォルダーがソース フォルダー ( _lpEntryID_で指定されたフォルダー) と同じ名前を持つ必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="50d41-120">[in] A pointer to the name of the copied or moved folder; otherwise, NULL, which indicates that the copied or moved folder should have the same name as the source folder (the folder pointed to by  _lpEntryID_).</span></span>
    
 <span data-ttu-id="50d41-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="50d41-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="50d41-122">[in]進行状況インジケーターのダイアログ ボックスのウィンドウと関連するウィンドウのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="50d41-122">[in] A handle of the window for the progress indicator dialog box and related windows.</span></span> <span data-ttu-id="50d41-123">_UlFlags_パラメーターに FOLDER_DIALOG フラグが設定されていない限り、 _ulUIParam_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="50d41-123">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="50d41-124">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="50d41-124">_lpProgress_</span></span>
  
> <span data-ttu-id="50d41-125">[in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="50d41-125">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="50d41-126">_LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="50d41-126">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="50d41-127">_UlFlags_に FOLDER_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="50d41-127">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="50d41-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="50d41-128">_ulFlags_</span></span>
  
> <span data-ttu-id="50d41-129">[in]コピーまたは移動操作を実現する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="50d41-129">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="50d41-130">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="50d41-130">The following flags can be set:</span></span>
    
<span data-ttu-id="50d41-131">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="50d41-131">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="50d41-132">すべてのフォルダーのサブフォルダーは、コピーまたは移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50d41-132">All of the folder's subfolders should be copied or moved.</span></span> <span data-ttu-id="50d41-133">コピー操作のために COPY_SUBFOLDERS が設定されていない場合は、 _lpEntryID_によって識別されたフォルダーのみがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="50d41-133">When COPY_SUBFOLDERS is not set for a copy operation, only the folder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="50d41-134">移動操作で、COPY_SUBFOLDERS の動作は既定のフラグが設定されているかどうかに関係なくです。</span><span class="sxs-lookup"><span data-stu-id="50d41-134">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="50d41-135">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="50d41-135">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="50d41-136">進行状況インジケーターの表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="50d41-136">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="50d41-137">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="50d41-137">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="50d41-138">フォルダーの移動の代わりにコピーします。</span><span class="sxs-lookup"><span data-stu-id="50d41-138">The folder should be moved instead of copied.</span></span> <span data-ttu-id="50d41-139">FOLDER_MOVE が設定されていない場合、フォルダーをコピーします。</span><span class="sxs-lookup"><span data-stu-id="50d41-139">If FOLDER_MOVE is not set, the folder is copied.</span></span>
    
<span data-ttu-id="50d41-140">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50d41-140">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="50d41-141">フォルダーの名前は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="50d41-141">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="50d41-142">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のフォルダーの名前です。</span><span class="sxs-lookup"><span data-stu-id="50d41-142">If the MAPI_UNICODE flag is not set, the name of the folder is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="50d41-143">�߂�l</span><span class="sxs-lookup"><span data-stu-id="50d41-143">Return value</span></span>

<span data-ttu-id="50d41-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="50d41-144">S_OK</span></span> 
  
> <span data-ttu-id="50d41-145">フォルダーは正常にコピーまたは移動されています。</span><span class="sxs-lookup"><span data-stu-id="50d41-145">The folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="50d41-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="50d41-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="50d41-147">移動またはコピーされているフォルダーの名前は、コピー先のフォルダーのサブフォルダーの名前と同じです。</span><span class="sxs-lookup"><span data-stu-id="50d41-147">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="50d41-148">メッセージ ストア プロバイダーは、フォルダー名が一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="50d41-148">The message store provider requires that folder names be unique.</span></span> <span data-ttu-id="50d41-149">完了せず、操作を停止します。</span><span class="sxs-lookup"><span data-stu-id="50d41-149">The operation stops without completing.</span></span>
    
<span data-ttu-id="50d41-150">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="50d41-150">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="50d41-151">呼び出しが成功したが、すべてのエントリが正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="50d41-151">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="50d41-152">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50d41-152">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="50d41-153">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="50d41-153">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="50d41-154">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50d41-154">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50d41-155">注釈</span><span class="sxs-lookup"><span data-stu-id="50d41-155">Remarks</span></span>

<span data-ttu-id="50d41-156">メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::CopyFolder**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="50d41-156">The **IMAPISupport::CopyFolder** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="50d41-157">メッセージ ストア プロバイダーは、コピーまたは別の 1 つの親フォルダーから 1 つのフォルダーを移動する[IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)の実装では、 **IMAPISupport::CopyFolder**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="50d41-157">Message store providers can call **IMAPISupport::CopyFolder** in their implementation of [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) to copy or move a single folder from one parent folder to another.</span></span> 
  
 <span data-ttu-id="50d41-158">**IMAPISupport::CopyFolder**は、コピー先のフォルダーのサブフォルダーとしてコピーまたは移動したフォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="50d41-158">**IMAPISupport::CopyFolder** adds the copied or moved folder as a subfolder of the destination folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="50d41-159">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="50d41-159">Notes to callers</span></span>

 <span data-ttu-id="50d41-160">**IMAPISupport::CopyFolder**は、名前を変更してフォルダーと、コピーまたは移動の影響を受けるフォルダーのサブフォルダーの移動を同時に使用できます。</span><span class="sxs-lookup"><span data-stu-id="50d41-160">**IMAPISupport::CopyFolder** allows simultaneous renaming and moving of folders and the copying or moving of subfolders of the affected folder.</span></span> <span data-ttu-id="50d41-161">コピーまたは移動、コピーまたは移動したフォルダーにネストされたすべてのサブフォルダー、 _ulFlags_で COPY_SUBFOLDERS フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="50d41-161">To copy or move all subfolders nested in the copied or moved folder, pass the COPY_SUBFOLDERS flag in  _ulFlags_.</span></span> 
  
<span data-ttu-id="50d41-162">次に、次の条件の値を返すことを期待される結果します。</span><span class="sxs-lookup"><span data-stu-id="50d41-162">Expect the following return values under the following conditions:</span></span>
  
|<span data-ttu-id="50d41-163">**条件**</span><span class="sxs-lookup"><span data-stu-id="50d41-163">**Condition**</span></span>|<span data-ttu-id="50d41-164">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="50d41-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="50d41-165">**CopyFolder**は正常にコピーまたは適用可能な場合、フォルダーとそのすべてのサブフォルダーを移動します。</span><span class="sxs-lookup"><span data-stu-id="50d41-165">**CopyFolder** successfully copied or moved the folder and all its subfolders, if applicable.</span></span>  <br/> |<span data-ttu-id="50d41-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="50d41-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="50d41-167">**CopyFolder**は、正常にコピーまたはすべてのフォルダーを移動できませんでした。</span><span class="sxs-lookup"><span data-stu-id="50d41-167">**CopyFolder** was unable to successfully copy or move all of the folders.</span></span>  <br/> |<span data-ttu-id="50d41-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="50d41-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="50d41-169">**CopyFolder**は完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="50d41-169">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="50d41-170">エラー値</span><span class="sxs-lookup"><span data-stu-id="50d41-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="50d41-171">**CopyFolder**では、エラー値が返された場合は、作業が実行されなかったことを想定しては続行できません。</span><span class="sxs-lookup"><span data-stu-id="50d41-171">If **CopyFolder** returns an error value, do not proceed on the assumption that no work was done.</span></span> <span data-ttu-id="50d41-172">1 つまたは複数のフォルダーでしたコピーされたり、 **CopyFolder**にエラーが発生した前に移動します。</span><span class="sxs-lookup"><span data-stu-id="50d41-172">One or more folders could have been copied or moved before **CopyFolder** experienced the failure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50d41-173">関連項目</span><span class="sxs-lookup"><span data-stu-id="50d41-173">See also</span></span>



[<span data-ttu-id="50d41-174">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="50d41-174">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

