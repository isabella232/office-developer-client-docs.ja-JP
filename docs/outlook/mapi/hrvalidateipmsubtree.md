---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436574"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="ffe7b-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="ffe7b-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="ffe7b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffe7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffe7b-105">標準の対人間メッセージ (IPM) フォルダーをメッセージ ストアに追加します。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ffe7b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ffe7b-106">Header file:</span></span>  <br/> |<span data-ttu-id="ffe7b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ffe7b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ffe7b-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="ffe7b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ffe7b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ffe7b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ffe7b-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ffe7b-110">Called by:</span></span>  <br/> |<span data-ttu-id="ffe7b-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="ffe7b-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="ffe7b-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ffe7b-112">Parameters</span></span>

 <span data-ttu-id="ffe7b-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="ffe7b-113">_lpMDB_</span></span>
  
> <span data-ttu-id="ffe7b-114">[in]フォルダーを追加するメッセージ ストア オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="ffe7b-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ffe7b-115">_ulFlags_</span></span>
  
> <span data-ttu-id="ffe7b-116">[in]フォルダーの作成方法を制御するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="ffe7b-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-117">The following flags can be set:</span></span>
    
<span data-ttu-id="ffe7b-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="ffe7b-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="ffe7b-119">メッセージ ストアのプロパティで有効なフォルダーが示されている場合でも、作成前にフォルダーを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="ffe7b-120">通常、クライアント アプリケーションは、既存のフォルダーの構造が破損しているというエラーが表示される場合に、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="ffe7b-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="ffe7b-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="ffe7b-122">IPM フォルダーの完全なセットは、メッセージ ストアのルート フォルダーに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="ffe7b-123">階層内のフォルダー タイトルは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="ffe7b-124">フォルダー ビュー</span><span class="sxs-lookup"><span data-stu-id="ffe7b-124">Folder Views</span></span>
    
    - <span data-ttu-id="ffe7b-125">共通ビュー</span><span class="sxs-lookup"><span data-stu-id="ffe7b-125">Common Views</span></span>
    
    - <span data-ttu-id="ffe7b-126">検索ルート\*</span><span class="sxs-lookup"><span data-stu-id="ffe7b-126">Search Root\*</span></span>
    
    - <span data-ttu-id="ffe7b-127">IPM サブツリー\*</span><span class="sxs-lookup"><span data-stu-id="ffe7b-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="ffe7b-128">受信トレイ</span><span class="sxs-lookup"><span data-stu-id="ffe7b-128">Inbox</span></span>
    
    - <span data-ttu-id="ffe7b-129">送信トレイ</span><span class="sxs-lookup"><span data-stu-id="ffe7b-129">Outbox</span></span>
    
    - <span data-ttu-id="ffe7b-130">削除済みアイテム\*</span><span class="sxs-lookup"><span data-stu-id="ffe7b-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="ffe7b-131">送信済みアイテム</span><span class="sxs-lookup"><span data-stu-id="ffe7b-131">Sent Items</span></span>
    
    <span data-ttu-id="ffe7b-132">ここで、マークされた 3 つのフォルダーは、フラグが設定されていない場合でもMAPI_FULL_IPM_TREE \* 設定されます。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="ffe7b-133">通常、クライアント アプリケーションは、フォルダーを作成するメッセージ ストアが既定のストアである場合に、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="ffe7b-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="ffe7b-134">_lpcValues_</span></span>
  
> <span data-ttu-id="ffe7b-135">[in, out]_lppProps_ パラメーターで返される配列内の [SPropValue](spropvalue.md)構造体の数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="ffe7b-136">_lppProps が NULL の場合は、lpcValues_ パラメーターの値を _0_ にできます。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="ffe7b-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="ffe7b-137">_lppProps_</span></span>
  
> <span data-ttu-id="ffe7b-138">[in, out]**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) プロパティおよび適切なフォルダー エントリ識別子プロパティのプロパティ値を含む **SPropValue** 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="ffe7b-139">**HrValidateIPMSubtree** がメッセージ ストアに受信トレイを作成する場合 **、SPropValue** 配列には、 としてコード化された特別なプロパティ タグを持つ受信トレイエントリ識別子が含まれます `PROP_TAG(PT_BINARY, PROP_ID_NULL)` 。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="ffe7b-140">_lppProps_ パラメーターには NULL を指定できます。呼び出し元の実装で **SPropValue** 配列を返す必要がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="ffe7b-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="ffe7b-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="ffe7b-142">[out]エラーのバージョン、コンポーネント、コンテキスト情報を含む [MAPIERROR](mapierror.md) 構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="ffe7b-143">_MAPIERROR 構造体が返されない場合、lppMAPIError_ パラメーターは **NULL** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ffe7b-144">Return value</span><span class="sxs-lookup"><span data-stu-id="ffe7b-144">Return value</span></span>

<span data-ttu-id="ffe7b-145">なし。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ffe7b-146">注釈</span><span class="sxs-lookup"><span data-stu-id="ffe7b-146">Remarks</span></span>

<span data-ttu-id="ffe7b-147">MAPI は **、HrValidateIPMSubtree** 関数を内部的に使用して、ストアを最初に開いた場合、またはストアが既定のストアにされた場合に、メッセージ ストアに標準 IPM サブツリーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="ffe7b-148">この関数は、クライアント アプリケーションで標準のメッセージ フォルダーを検証または修復するためにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="ffe7b-149">**HrValidateIPMSubtree** は常に、ストアのルート フォルダーに検索ルート フォルダーと IPM サブツリー フォルダー、IPM サブツリー フォルダーに [削除済みアイテム] フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="ffe7b-150">IPM サブツリー フォルダーは、そのメッセージ ストア内の IPM 階層のルートです。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="ffe7b-151">検索ルート フォルダーは、検索結果フォルダーのサブツリーのルートとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="ffe7b-152">IPM クライアントは、IPM サブツリー ルート フォルダーから開始し、その下に子フォルダーを表示するフォルダー ビューを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="ffe7b-153">メッセージ ストアのルート フォルダー内の情報は、クライアントのユーザー インターフェイスに表示されません。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="ffe7b-154">この機能は、クライアントが情報を非表示にする必要がある場合、情報を IPM サブツリー ルート ディレクトリに置き、ユーザーに表示されない場所に置く可能性を意味します。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="ffe7b-155">これに対し、サーバー ベースのメッセージ ストアなど、メッセージとフォルダーをユーザーに表示しない必要がある IPM 以外のアプリケーションでは、IPM 階層の外側に置く可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="ffe7b-156">**HrValidateIPMSubtree** は **、PR_VALID_FOLDER_MASK** プロパティを設定して、作成する各 IPM フォルダーに有効なエントリ識別子が設定されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="ffe7b-157">メッセージ ストアの次のエントリ識別子プロパティは、対応するフォルダーのエントリ識別子に設定され _、lppProps_ パラメーターと共に次の **PR_VALID_FOLDER_MASK。**</span><span class="sxs-lookup"><span data-stu-id="ffe7b-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="ffe7b-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ffe7b-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="ffe7b-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ffe7b-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="ffe7b-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ffe7b-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="ffe7b-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ffe7b-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="ffe7b-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ffe7b-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="ffe7b-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ffe7b-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="ffe7b-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ffe7b-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="ffe7b-165">IPM 受信 [PROP_TAG](prop_tag.md) のプレースホルダー (PT_BINARY、PROP_ID_NULL)。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="ffe7b-166">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="ffe7b-166">MFCMAPI reference</span></span>

<span data-ttu-id="ffe7b-167">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ffe7b-168">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="ffe7b-168">**File**</span></span>|<span data-ttu-id="ffe7b-169">**関数**</span><span class="sxs-lookup"><span data-stu-id="ffe7b-169">**Function**</span></span>|<span data-ttu-id="ffe7b-170">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ffe7b-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ffe7b-171">MstStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ffe7b-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="ffe7b-172">CMsgStoreDlg::OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="ffe7b-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="ffe7b-173">MFCMAPI は **、HrValidateIPMSubtree** メソッドを使用して、標準フォルダーをメッセージ ストアに追加します。</span><span class="sxs-lookup"><span data-stu-id="ffe7b-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ffe7b-174">関連項目</span><span class="sxs-lookup"><span data-stu-id="ffe7b-174">See also</span></span>



[<span data-ttu-id="ffe7b-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="ffe7b-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


<span data-ttu-id="ffe7b-176">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ffe7b-176">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

