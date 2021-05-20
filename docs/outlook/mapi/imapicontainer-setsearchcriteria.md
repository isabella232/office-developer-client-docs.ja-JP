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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427200"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="6fb44-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="6fb44-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="6fb44-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fb44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fb44-105">コンテナーの検索条件を設定します。</span><span class="sxs-lookup"><span data-stu-id="6fb44-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6fb44-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6fb44-106">Parameters</span></span>

 <span data-ttu-id="6fb44-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="6fb44-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="6fb44-108">[in]検索条件を [定義する SRestriction](srestriction.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6fb44-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="6fb44-109">_lpRestriction_ パラメーターで NULL が渡された場合、このコンテナーで最近使用された検索条件が再び使用されます。</span><span class="sxs-lookup"><span data-stu-id="6fb44-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="6fb44-110">コンテナー内の最初の検索  _では、lpRestriction_ で NULL を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fb44-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="6fb44-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="6fb44-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="6fb44-112">[in]検索に含めるコンテナーを表すエントリ識別子の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6fb44-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="6fb44-113">クライアントが  _lpContainerList_ パラメーターで NULL を渡した場合、このコンテナーの検索に最近使用されたエントリ識別子が新しい検索に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6fb44-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="6fb44-114">クライアントは、コンテナー内の最初の検索に  _lpContainerList_ で NULL を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fb44-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="6fb44-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="6fb44-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="6fb44-116">[in]検索の実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="6fb44-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="6fb44-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6fb44-117">The following flags can be set:</span></span>
    
<span data-ttu-id="6fb44-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="6fb44-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="6fb44-119">検索は、他の検索に対する通常の優先度で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fb44-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="6fb44-120">このフラグは、このフラグと同時に設定FOREGROUND_SEARCHできません。</span><span class="sxs-lookup"><span data-stu-id="6fb44-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="6fb44-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="6fb44-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="6fb44-122">検索は、他の検索と相対的に高い優先度で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fb44-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="6fb44-123">このフラグは、このフラグと同時に設定BACKGROUND_SEARCHできません。</span><span class="sxs-lookup"><span data-stu-id="6fb44-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="6fb44-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="6fb44-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="6fb44-125">一致するエントリを検索する場合は、コンテンツ インデックスを使用しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fb44-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="6fb44-126">このフラグは、一部のストアExchangeです。</span><span class="sxs-lookup"><span data-stu-id="6fb44-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="6fb44-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="6fb44-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="6fb44-128">検索には  _、lpContainerList_ パラメーターで指定されたコンテナーとそのすべての子コンテナーが含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fb44-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="6fb44-129">このフラグは、このフラグと同時に設定SHALLOW_SEARCHできません。</span><span class="sxs-lookup"><span data-stu-id="6fb44-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="6fb44-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="6fb44-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="6fb44-131">**これが SetSearchCriteria** への最初の呼び出しである場合は検索を開始するか、検索が非アクティブな場合は再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fb44-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="6fb44-132">このフラグは、このフラグと同時に設定STOP_SEARCHできません。</span><span class="sxs-lookup"><span data-stu-id="6fb44-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="6fb44-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="6fb44-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="6fb44-134">検索は、一致するエントリの  _lpContainerList_ パラメーターで指定されたコンテナーでのみ検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fb44-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="6fb44-135">このフラグは、このフラグと同時に設定RECURSIVE_SEARCHできません。</span><span class="sxs-lookup"><span data-stu-id="6fb44-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="6fb44-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="6fb44-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="6fb44-137">検索を停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fb44-137">The search should be stopped.</span></span> <span data-ttu-id="6fb44-138">このフラグは、このフラグと同時に設定RESTART_SEARCHできません。</span><span class="sxs-lookup"><span data-stu-id="6fb44-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6fb44-139">戻り値</span><span class="sxs-lookup"><span data-stu-id="6fb44-139">Return value</span></span>

<span data-ttu-id="6fb44-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="6fb44-140">S_OK</span></span> 
  
> <span data-ttu-id="6fb44-141">検索条件が正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="6fb44-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="6fb44-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="6fb44-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="6fb44-143">サービス プロバイダーは、指定された検索条件をサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="6fb44-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6fb44-144">注釈</span><span class="sxs-lookup"><span data-stu-id="6fb44-144">Remarks</span></span>

<span data-ttu-id="6fb44-145">**IMAPIContainer::SetSearchCriteria** メソッドは、検索をサポートするコンテナー (通常は検索結果フォルダー) の検索条件を確立します。</span><span class="sxs-lookup"><span data-stu-id="6fb44-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="6fb44-146">検索結果フォルダーには、検索条件を満たすメッセージへのリンクが含まれます。実際のメッセージは、元の場所に保存されます。</span><span class="sxs-lookup"><span data-stu-id="6fb44-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="6fb44-147">検索結果フォルダーに含まれる唯一の一意のデータは、そのコンテンツ テーブルです。</span><span class="sxs-lookup"><span data-stu-id="6fb44-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="6fb44-148">検索結果フォルダーのコンテンツ テーブルには、検索制限が適用された後に、メッセージ ストアの結合されたコンテンツがあります。</span><span class="sxs-lookup"><span data-stu-id="6fb44-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="6fb44-149">検索操作は、この結合されたコンテンツ テーブルでのみ機能します。他の検索結果フォルダーを検索しない。</span><span class="sxs-lookup"><span data-stu-id="6fb44-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="6fb44-150">検索結果は、検索条件に一致するメッセージのみを返します。フォルダー階層は返されません。</span><span class="sxs-lookup"><span data-stu-id="6fb44-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="6fb44-151">検索が完了すると、コントロールがクライアントに返されます。</span><span class="sxs-lookup"><span data-stu-id="6fb44-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6fb44-152">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="6fb44-152">Notes to implementers</span></span>

<span data-ttu-id="6fb44-153">アドレス帳コンテナーは、コンテンツ テーブルに制限を適用して検索条件を確立します。</span><span class="sxs-lookup"><span data-stu-id="6fb44-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="6fb44-154">検索条件とアドレス帳コンテナーの詳細については、「高度な検索の実装 [」を参照してください](implementing-advanced-searching.md)。</span><span class="sxs-lookup"><span data-stu-id="6fb44-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="6fb44-155">検索結果フォルダー自体ではなく、検索結果フォルダー内のメッセージに対する開く、コピー、移動、削除の操作をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fb44-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="6fb44-156">メッセージを検索結果フォルダー内に作成したり、検索結果フォルダーにコピーしたりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6fb44-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6fb44-157">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="6fb44-157">Notes to callers</span></span>

<span data-ttu-id="6fb44-158">メッセージ受信者を検索するには _、sSubRestriction_ 構造体の **ulSubObject** メンバーが PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)に設定されたサブオブジェクト制限をポイントする [lpRestriction](ssubrestriction.md)を設定します。 </span><span class="sxs-lookup"><span data-stu-id="6fb44-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="6fb44-159">添付ファイルを検索するには **、ulSubObject** **メンバー** を PR_MESSAGE_ATTACHMENTS ([PidTagMessageAttachments) に設定します](pidtagmessageattachments-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="6fb44-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="6fb44-160">**lpRes メンバーに**、受信者または添付ファイルの検索条件を示すプロパティ制限を指定します。</span><span class="sxs-lookup"><span data-stu-id="6fb44-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="6fb44-161">たとえば、拡張子が .mss の添付ファイルを検索するには **、ulSubObject** を **PR_MESSAGE_ATTACHMENTS** に **、lpRes** を **、.mss** の PR_ATTACH_EXTENSION ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) と一致するプロパティ制限に設定します。</span><span class="sxs-lookup"><span data-stu-id="6fb44-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="6fb44-162">_ulSearchFlags_ パラメーター FOREGROUND_SEARCHフラグを設定すると、システムのパフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6fb44-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="6fb44-163">**SetSearchCriteria を使用して**、既に進行中の検索の検索条件を変更できます。</span><span class="sxs-lookup"><span data-stu-id="6fb44-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="6fb44-164">新しい制限、検索するフォルダーの新しいリスト、および検索の優先度を高くするなどの新しい検索優先度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6fb44-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="6fb44-165">検索優先度の変更によって既存の検索が再開されるのではなく、検索条件に対するその他の変更が可能です。</span><span class="sxs-lookup"><span data-stu-id="6fb44-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="6fb44-166">検索結果フォルダーを使用している場合は、フォルダーを削除するか、後で使用するために開いたままにできます。</span><span class="sxs-lookup"><span data-stu-id="6fb44-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="6fb44-167">検索結果フォルダーを削除すると、メッセージ リンクだけが削除されます。</span><span class="sxs-lookup"><span data-stu-id="6fb44-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="6fb44-168">実際のメッセージは親フォルダーに残ります。</span><span class="sxs-lookup"><span data-stu-id="6fb44-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="6fb44-169">検索結果フォルダーの詳細については、「MAPI 検索フォルダー [」を参照してください](mapi-search-folders.md)。</span><span class="sxs-lookup"><span data-stu-id="6fb44-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6fb44-170">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="6fb44-170">MFCMAPI reference</span></span>

<span data-ttu-id="6fb44-171">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6fb44-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6fb44-172">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="6fb44-172">**File**</span></span>|<span data-ttu-id="6fb44-173">**関数**</span><span class="sxs-lookup"><span data-stu-id="6fb44-173">**Function**</span></span>|<span data-ttu-id="6fb44-174">**コメント**</span><span class="sxs-lookup"><span data-stu-id="6fb44-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6fb44-175">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6fb44-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="6fb44-176">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="6fb44-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="6fb44-177">MFCMAPI は **IMAPIContainer::SetSearchCriteria** メソッドを使用して、ユーザーがフォルダーを編集した後にフォルダーの検索条件を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="6fb44-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6fb44-178">関連項目</span><span class="sxs-lookup"><span data-stu-id="6fb44-178">See also</span></span>



[<span data-ttu-id="6fb44-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="6fb44-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="6fb44-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6fb44-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="6fb44-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="6fb44-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="6fb44-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="6fb44-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="6fb44-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="6fb44-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="6fb44-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="6fb44-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="6fb44-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="6fb44-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="6fb44-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6fb44-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


<span data-ttu-id="6fb44-187">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="6fb44-187">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

