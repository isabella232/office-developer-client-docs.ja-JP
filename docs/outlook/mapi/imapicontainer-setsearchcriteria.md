---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350968"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="3f6ff-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="3f6ff-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="3f6ff-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f6ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f6ff-105">コンテナーの検索条件を確立します。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3f6ff-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3f6ff-106">Parameters</span></span>

 <span data-ttu-id="3f6ff-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="3f6ff-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="3f6ff-108">順番検索条件を定義する[srestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="3f6ff-109">_lpRestriction_パラメーターで NULL が渡された場合、このコンテナーに対して最近使用された検索条件が再度使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="3f6ff-110">コンテナー内の最初の検索では、 _lpRestriction_で NULL を渡すことはできません。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="3f6ff-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="3f6ff-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="3f6ff-112">順番検索に含めるコンテナーを表すエントリ識別子の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="3f6ff-113">クライアントが_lpContainerList_パラメーターで NULL を渡した場合、最近このコンテナーを検索するために使用されたエントリ識別子が新しい検索に使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="3f6ff-114">コンテナー内の最初の検索では、クライアントは_lpContainerList_で NULL を渡さないでください。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="3f6ff-115">_ulsearchflags_</span><span class="sxs-lookup"><span data-stu-id="3f6ff-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="3f6ff-116">順番検索の実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="3f6ff-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-117">The following flags can be set:</span></span>
    
<span data-ttu-id="3f6ff-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="3f6ff-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="3f6ff-119">検索は、他の検索と比較して標準の優先度で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="3f6ff-120">このフラグは、FOREGROUND_SEARCH フラグと同時には設定できません。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="3f6ff-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="3f6ff-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="3f6ff-122">検索は、他の検索と比較して高い優先度で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="3f6ff-123">このフラグは、BACKGROUND_SEARCH フラグと同時には設定できません。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="3f6ff-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="3f6ff-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="3f6ff-125">検索では、一致するエントリを検索するために、コンテンツインデックスを使用しません。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="3f6ff-126">このフラグは、Exchange ストアに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="3f6ff-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="3f6ff-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="3f6ff-128">検索には、 _lpContainerList_パラメーターとそのすべての子コンテナーで指定されたコンテナーが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="3f6ff-129">このフラグは、SHALLOW_SEARCH フラグと同時には設定できません。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="3f6ff-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="3f6ff-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="3f6ff-131">この検索は、 **setsearchcriteria**の最初の呼び出しである場合に開始するか、または検索が非アクティブな場合に再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="3f6ff-132">このフラグは、STOP_SEARCH フラグと同時には設定できません。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="3f6ff-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="3f6ff-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="3f6ff-134">検索は、一致するエントリに対して_lpContainerList_パラメーターで指定されたコンテナー内のみを参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="3f6ff-135">このフラグは、RECURSIVE_SEARCH フラグと同時には設定できません。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="3f6ff-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="3f6ff-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="3f6ff-137">検索を停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-137">The search should be stopped.</span></span> <span data-ttu-id="3f6ff-138">このフラグは、RESTART_SEARCH フラグと同時には設定できません。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3f6ff-139">戻り値</span><span class="sxs-lookup"><span data-stu-id="3f6ff-139">Return value</span></span>

<span data-ttu-id="3f6ff-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f6ff-140">S_OK</span></span> 
  
> <span data-ttu-id="3f6ff-141">検索条件が正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="3f6ff-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="3f6ff-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="3f6ff-143">サービスプロバイダーは、指定された検索条件をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f6ff-144">解説</span><span class="sxs-lookup"><span data-stu-id="3f6ff-144">Remarks</span></span>

<span data-ttu-id="3f6ff-145">**IMAPIContainer:: setsearchcriteria**メソッドは、検索をサポートするコンテナー (通常は検索結果フォルダー) の検索条件を設定します。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="3f6ff-146">検索結果フォルダーには、検索条件に一致するメッセージへのリンクが含まれています。実際のメッセージは、元の場所に保存されたままになります。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="3f6ff-147">検索結果フォルダーに格納されている一意のデータは、[コンテンツ] テーブルだけです。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="3f6ff-148">検索結果フォルダーの contents テーブルには、検索制限が適用された後に、メッセージストアの内容がマージされています。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="3f6ff-149">検索操作は、この結合されたコンテンツテーブルでのみ動作します。他の検索結果フォルダーは検索されません。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="3f6ff-150">検索結果には、検索条件に一致するメッセージのみが返されます。フォルダー階層は返されません。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="3f6ff-151">検索が完了すると、コントロールはクライアントに返されます。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3f6ff-152">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="3f6ff-152">Notes to implementers</span></span>

<span data-ttu-id="3f6ff-153">アドレス帳コンテナーは、コンテンツテーブルに制限を適用して検索条件を確立します。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="3f6ff-154">検索条件とアドレス帳コンテナーの詳細については、「[高度な検索の実装](implementing-advanced-searching.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="3f6ff-155">検索結果フォルダー自体ではなく、検索結果フォルダー内のメッセージに対して、オープン、コピー、移動、および削除の操作をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="3f6ff-156">検索結果フォルダー内でのメッセージの作成またはコピーを許可しません。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3f6ff-157">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="3f6ff-157">Notes to callers</span></span>

<span data-ttu-id="3f6ff-158">メッセージの受信者を検索するには、 [ssubrestriction](ssubrestriction.md)構造で**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) に設定されている ulsubmember を持つサブ要素制限を指すように\*\*\*\* _lpRestriction_を設定します。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="3f6ff-159">添付ファイルを検索するには\*\*\*\* 、ulsubobject メンバーを**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) に設定します。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="3f6ff-160">受信者または添付ファイルの検索条件を記述するプロパティ制限をポイントするように、 **lpres**メンバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="3f6ff-161">たとえば、拡張子が mss の添付ファイルを検索するには、ulsubobject \*\*\*\* を**PR_MESSAGE_ATTACHMENTS**および**lpres**に設定して、 **PR_ATTACH_EXTENSION**に一致するプロパティ制限に設定します ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) を使用します。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="3f6ff-162">_ulsearchflags_パラメーターに FOREGROUND_SEARCH フラグを設定すると、システムのパフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="3f6ff-163">**setsearchcriteria**を使用して、既に進行中の検索条件を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="3f6ff-164">新しい制限を指定したり、検索するフォルダーの新しいリストを指定したり、検索をより高い優先度にアップグレードするなどの新しい検索の優先度を指定したりできます。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="3f6ff-165">検索優先度の変更によって既存の検索が再起動されることはありませんが、検索条件に対するその他の変更はできません。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="3f6ff-166">検索結果フォルダーを使用している場合は、フォルダーを削除するか、または後で使用するために開いたままにしておくことができます。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="3f6ff-167">検索結果フォルダーを削除すると、メッセージリンクのみが削除されます。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="3f6ff-168">実際のメッセージは親フォルダーに残ります。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="3f6ff-169">検索結果フォルダーの詳細については、「 [MAPI 検索フォルダー](mapi-search-folders.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3f6ff-170">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="3f6ff-170">MFCMAPI reference</span></span>

<span data-ttu-id="3f6ff-171">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3f6ff-172">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="3f6ff-172">**File**</span></span>|<span data-ttu-id="3f6ff-173">**関数**</span><span class="sxs-lookup"><span data-stu-id="3f6ff-173">**Function**</span></span>|<span data-ttu-id="3f6ff-174">**コメント**</span><span class="sxs-lookup"><span data-stu-id="3f6ff-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3f6ff-175">HierarchyTableDlg</span><span class="sxs-lookup"><span data-stu-id="3f6ff-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="3f6ff-176">CHierarchyTableDlg:: oneditsearchcriteria</span><span class="sxs-lookup"><span data-stu-id="3f6ff-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="3f6ff-177">mfcmapi は、 **IMAPIContainer:: setsearchcriteria**メソッドを使用して、ユーザーが編集した後のフォルダーの検索条件を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="3f6ff-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f6ff-178">関連項目</span><span class="sxs-lookup"><span data-stu-id="3f6ff-178">See also</span></span>



[<span data-ttu-id="3f6ff-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="3f6ff-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="3f6ff-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3f6ff-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="3f6ff-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="3f6ff-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="3f6ff-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3f6ff-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="3f6ff-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="3f6ff-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="3f6ff-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="3f6ff-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="3f6ff-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="3f6ff-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="3f6ff-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3f6ff-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


<span data-ttu-id="3f6ff-187">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="3f6ff-187">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

