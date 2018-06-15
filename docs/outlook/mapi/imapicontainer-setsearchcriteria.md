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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 93578300e2520dda4a9621b05ac6a79c54eca2ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800462"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="c38c6-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="c38c6-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="c38c6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c38c6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c38c6-105">コンテナーの検索基準を確立します。</span><span class="sxs-lookup"><span data-stu-id="c38c6-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c38c6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c38c6-106">Parameters</span></span>

 <span data-ttu-id="c38c6-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="c38c6-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="c38c6-108">[in]検索条件を定義する[SRestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c38c6-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="c38c6-109">_LpRestriction_パラメーターに NULL を渡した場合、このコンテナーの最も最近使用した検索条件が再度使用されます。</span><span class="sxs-lookup"><span data-stu-id="c38c6-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="c38c6-110">NULL 渡すことはできません_lpRestriction_のコンテナー内の最初の検索をします。</span><span class="sxs-lookup"><span data-stu-id="c38c6-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="c38c6-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="c38c6-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="c38c6-112">[in]検索に含まれるコンテナーを表すエントリの識別子の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c38c6-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="c38c6-113">_LpContainerList_パラメーターに NULL を渡すと、クライアント、新しい検索のこのコンテナーを検索するのには最近使った項目識別子が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c38c6-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="c38c6-114">クライアントは、コンテナー内の最初の検索の_lpContainerList_に NULL を渡さないでください。</span><span class="sxs-lookup"><span data-stu-id="c38c6-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="c38c6-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="c38c6-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="c38c6-116">[in]検索の実行方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="c38c6-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="c38c6-117">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c38c6-117">The following flags can be set:</span></span>
    
<span data-ttu-id="c38c6-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="c38c6-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="c38c6-119">検索は、他の検索基準にして通常の優先順位で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c38c6-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="c38c6-120">FOREGROUND_SEARCH フラグと同時には、このフラグを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="c38c6-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="c38c6-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="c38c6-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="c38c6-122">検索は、他の検索基準とした優先度の高いで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c38c6-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="c38c6-123">BACKGROUND_SEARCH フラグと同時には、このフラグを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="c38c6-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="c38c6-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="c38c6-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="c38c6-125">検索使用しないでくださいコンテンツのインデックス作成に一致するエントリを検索します。</span><span class="sxs-lookup"><span data-stu-id="c38c6-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="c38c6-126">このフラグで、Exchange ストアに対してのみです。</span><span class="sxs-lookup"><span data-stu-id="c38c6-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="c38c6-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="c38c6-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="c38c6-128">検索では、 _lpContainerList_パラメーターとそのすべての子コンテナーで指定されたコンテナーを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="c38c6-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="c38c6-129">SHALLOW_SEARCH フラグと同時には、このフラグを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="c38c6-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="c38c6-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="c38c6-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="c38c6-131">検索は、これは、 **SetSearchCriteria**、最初の呼び出しを開始または検索がアクティブでない場合に再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c38c6-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="c38c6-132">STOP_SEARCH フラグと同時には、このフラグを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="c38c6-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="c38c6-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="c38c6-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="c38c6-134">検索に一致するエントリの_lpContainerList_パラメーターで指定したコンテナーでのみです。</span><span class="sxs-lookup"><span data-stu-id="c38c6-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="c38c6-135">RECURSIVE_SEARCH フラグと同時には、このフラグを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="c38c6-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="c38c6-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="c38c6-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="c38c6-137">検索を停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c38c6-137">The search should be stopped.</span></span> <span data-ttu-id="c38c6-138">RESTART_SEARCH フラグと同時には、このフラグを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="c38c6-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c38c6-139">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c38c6-139">Return value</span></span>

<span data-ttu-id="c38c6-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="c38c6-140">S_OK</span></span> 
  
> <span data-ttu-id="c38c6-141">検索条件が正しく設定されました。</span><span class="sxs-lookup"><span data-stu-id="c38c6-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="c38c6-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="c38c6-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="c38c6-143">サービス プロバイダーは、指定された検索条件をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c38c6-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c38c6-144">Remarks</span><span class="sxs-lookup"><span data-stu-id="c38c6-144">Remarks</span></span>

<span data-ttu-id="c38c6-145">**IMAPIContainer::SetSearchCriteria**メソッドは、通常の検索結果フォルダーの検索をサポートするコンテナーの検索基準を確立します。</span><span class="sxs-lookup"><span data-stu-id="c38c6-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="c38c6-146">検索結果フォルダーには、検索条件に一致するメッセージへのリンクが含まれています。実際のメッセージは、元の場所に保存されています。</span><span class="sxs-lookup"><span data-stu-id="c38c6-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="c38c6-147">検索結果のフォルダーに含まれているのみに固有のデータは、その内容のテーブルです。</span><span class="sxs-lookup"><span data-stu-id="c38c6-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="c38c6-148">検索結果フォルダーの内容のテーブルでは、検索の制限が適用された後にメッセージ ・ ストアがマージされた内容があります。</span><span class="sxs-lookup"><span data-stu-id="c38c6-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="c38c6-149">検索操作は、この内容が結合されたテーブルでのみ動作します。他の検索結果のフォルダーを検索しません。</span><span class="sxs-lookup"><span data-stu-id="c38c6-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="c38c6-150">検索結果が検索条件に一致するメッセージのみを返すフォルダー階層は返されません。</span><span class="sxs-lookup"><span data-stu-id="c38c6-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="c38c6-151">検索が完了すると、制御がクライアントに返されます。</span><span class="sxs-lookup"><span data-stu-id="c38c6-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c38c6-152">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="c38c6-152">Notes to implementers</span></span>

<span data-ttu-id="c38c6-153">アドレス帳コンテナーは、その内容のテーブルに制限を適用することで検索条件を確立します。</span><span class="sxs-lookup"><span data-stu-id="c38c6-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="c38c6-154">詳細については検索条件とアドレス帳コンテナー、[高度な検索を実装する](implementing-advanced-searching.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c38c6-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="c38c6-155">必要がありますオープンをサポートして、コピー、移動、および削除の各操作の検索結果のフォルダー内のメッセージに、検索結果フォルダー自体ではなく。</span><span class="sxs-lookup"><span data-stu-id="c38c6-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="c38c6-156">内に作成または検索結果のフォルダーにコピーするメッセージを許可しません。</span><span class="sxs-lookup"><span data-stu-id="c38c6-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c38c6-157">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c38c6-157">Notes to callers</span></span>

<span data-ttu-id="c38c6-158">メッセージの受信者を検索するには、 **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) に設定する[SSubRestriction](ssubrestriction.md)構造体の**ulSubObject**メンバーとサブオブジェクトの制限] をポイントする_lpRestriction_を設定します。</span><span class="sxs-lookup"><span data-stu-id="c38c6-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="c38c6-159">添付ファイルを検索するには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) に**ulSubObject**のメンバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="c38c6-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="c38c6-160">受信者や添付ファイルの検索条件を記述するプロパティの制限] をポイントして、 **lpRes**のメンバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="c38c6-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="c38c6-161">たとえば、拡張子 .mss を含む添付ファイルを探すように**PR_MESSAGE_ATTACHMENTS**と**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)に一致するプロパティの制限を**lpRes**に**ulSubObject**を設定します。) を持つ。 mss。</span><span class="sxs-lookup"><span data-stu-id="c38c6-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="c38c6-162">_UlSearchFlags_パラメーターに FOREGROUND_SEARCH フラグを設定すると、システム パフォーマンスが低下可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c38c6-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="c38c6-163">既に進行中の検索の検索条件を変更するのには**SetSearchCriteria**を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c38c6-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="c38c6-164">新しい制限を検索するには、フォルダーと新しい検索の優先順位、優先度の高い検索にアップグレードするなどの新しいリストを指定できます。</span><span class="sxs-lookup"><span data-stu-id="c38c6-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="c38c6-165">検索の優先順位の変更を再起動して、既存の検索が発生しないが、条件を検索するには、その他の変更ができます。</span><span class="sxs-lookup"><span data-stu-id="c38c6-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="c38c6-166">検索結果フォルダーを使用するが、フォルダーを削除するか、後で使用するために開いたままにできるようにします。</span><span class="sxs-lookup"><span data-stu-id="c38c6-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="c38c6-167">検索結果フォルダーを削除すると、メッセージのリンクのみが削除されます。</span><span class="sxs-lookup"><span data-stu-id="c38c6-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="c38c6-168">実際のメッセージは、その親フォルダーに残ります。</span><span class="sxs-lookup"><span data-stu-id="c38c6-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="c38c6-169">検索結果フォルダーの詳細については、 [MAPI 検索フォルダー](mapi-search-folders.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c38c6-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c38c6-170">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="c38c6-170">MFCMAPI reference</span></span>

<span data-ttu-id="c38c6-171">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="c38c6-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c38c6-172">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="c38c6-172">**File**</span></span>|<span data-ttu-id="c38c6-173">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="c38c6-173">**Function**</span></span>|<span data-ttu-id="c38c6-174">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="c38c6-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c38c6-175">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c38c6-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="c38c6-176">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="c38c6-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="c38c6-177">MFCMAPI では、 **IMAPIContainer::SetSearchCriteria**メソッドを使用して、ユーザーがそれを編集した後、フォルダーの検索条件を記述します。</span><span class="sxs-lookup"><span data-stu-id="c38c6-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c38c6-178">関連項目</span><span class="sxs-lookup"><span data-stu-id="c38c6-178">See also</span></span>



[<span data-ttu-id="c38c6-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="c38c6-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="c38c6-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c38c6-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="c38c6-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="c38c6-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="c38c6-182">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c38c6-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="c38c6-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c38c6-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="c38c6-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="c38c6-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="c38c6-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="c38c6-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="c38c6-186">IMAPIContainer: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c38c6-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


<span data-ttu-id="c38c6-187">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c38c6-187">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

