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
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="342d2-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="342d2-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="342d2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="342d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="342d2-105">標準の個人間メッセージ (IPM) フォルダーをメッセージストアに追加します。</span><span class="sxs-lookup"><span data-stu-id="342d2-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="342d2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="342d2-106">Header file:</span></span>  <br/> |<span data-ttu-id="342d2-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="342d2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="342d2-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="342d2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="342d2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="342d2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="342d2-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="342d2-110">Called by:</span></span>  <br/> |<span data-ttu-id="342d2-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="342d2-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="342d2-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="342d2-112">Parameters</span></span>

 <span data-ttu-id="342d2-113">_lpmdb_</span><span class="sxs-lookup"><span data-stu-id="342d2-113">_lpMDB_</span></span>
  
> <span data-ttu-id="342d2-114">順番フォルダーを追加するメッセージストアオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="342d2-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="342d2-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="342d2-115">_ulFlags_</span></span>
  
> <span data-ttu-id="342d2-116">順番フォルダーの作成方法を制御するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="342d2-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="342d2-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="342d2-117">The following flags can be set:</span></span>
    
<span data-ttu-id="342d2-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="342d2-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="342d2-119">フォルダーは、メッセージストアのプロパティが有効であることを示している場合でも、作成前に確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="342d2-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="342d2-120">クライアントアプリケーションでは、通常、既存のフォルダーの構造が破損していることを示すエラーが発生すると、このフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="342d2-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="342d2-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="342d2-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="342d2-122">メッセージストアのルートフォルダーに、IPM フォルダーの完全なセットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="342d2-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="342d2-123">階層内のフォルダーのタイトルは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="342d2-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="342d2-124">フォルダービュー</span><span class="sxs-lookup"><span data-stu-id="342d2-124">Folder Views</span></span>
    
    - <span data-ttu-id="342d2-125">共通ビュー</span><span class="sxs-lookup"><span data-stu-id="342d2-125">Common Views</span></span>
    
    - <span data-ttu-id="342d2-126">検索ルート\*</span><span class="sxs-lookup"><span data-stu-id="342d2-126">Search Root\*</span></span>
    
    - <span data-ttu-id="342d2-127">IPM サブツリー\*</span><span class="sxs-lookup"><span data-stu-id="342d2-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="342d2-128">Inbox</span><span class="sxs-lookup"><span data-stu-id="342d2-128">Inbox</span></span>
    
    - <span data-ttu-id="342d2-129">送信トレイ</span><span class="sxs-lookup"><span data-stu-id="342d2-129">Outbox</span></span>
    
    - <span data-ttu-id="342d2-130">削除済みアイテム\*</span><span class="sxs-lookup"><span data-stu-id="342d2-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="342d2-131">送信済みアイテム</span><span class="sxs-lookup"><span data-stu-id="342d2-131">Sent Items</span></span>
    
    <span data-ttu-id="342d2-132">MAPI_FULL_IPM_TREE フラグが設定され\*ていない場合でも、ここでマークされている3つのフォルダーは、最小セットとして設定されます。</span><span class="sxs-lookup"><span data-stu-id="342d2-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="342d2-133">通常、クライアントアプリケーションは、フォルダーを作成するメッセージストアが既定のストアである場合に、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="342d2-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="342d2-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="342d2-134">_lpcValues_</span></span>
  
> <span data-ttu-id="342d2-135">[入力]_lppprops_パラメーターで返される配列内の[spropvalue](spropvalue.md)構造体の数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="342d2-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="342d2-136">_lppprops_が NULL の場合、 _lpcValues_パラメーターの値は0になります。</span><span class="sxs-lookup"><span data-stu-id="342d2-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="342d2-137">_lppprops_</span><span class="sxs-lookup"><span data-stu-id="342d2-137">_lppProps_</span></span>
  
> <span data-ttu-id="342d2-138">[入力]**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) プロパティのプロパティ値と、適切なフォルダーエントリ識別子のプロパティを含む**spropvalue**構造体の配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="342d2-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="342d2-139">**hrvalidateipmsubtree**がメッセージストア内に受信トレイを作成する場合、 **spropvalue**配列には、という`PROP_TAG(PT_BINARY, PROP_ID_NULL)`特殊なプロパティタグを持つ受信トレイエントリ識別子が含まれます。</span><span class="sxs-lookup"><span data-stu-id="342d2-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="342d2-140">_lppprops_パラメーターには NULL を指定できます。これは、呼び出し側の実装では、 **spropvalue**配列を返す必要がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="342d2-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="342d2-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="342d2-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="342d2-142">読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む[MAPIERROR](mapierror.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="342d2-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="342d2-143">**MAPIERROR**構造体が返されない場合、 _lppMAPIError_パラメーターは NULL に設定されます。</span><span class="sxs-lookup"><span data-stu-id="342d2-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="342d2-144">Return value</span><span class="sxs-lookup"><span data-stu-id="342d2-144">Return value</span></span>

<span data-ttu-id="342d2-145">なし。</span><span class="sxs-lookup"><span data-stu-id="342d2-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="342d2-146">注釈</span><span class="sxs-lookup"><span data-stu-id="342d2-146">Remarks</span></span>

<span data-ttu-id="342d2-147">MAPI は、ストアが最初に開かれたとき、またはストアが既定のストアになったときに、メッセージストアの標準の IPM サブツリーを構築するために、 **hrvalidateipmsubtree**関数を内部で使用します。</span><span class="sxs-lookup"><span data-stu-id="342d2-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="342d2-148">この関数は、クライアントアプリケーションが標準的なメッセージフォルダーを検証または修復するために使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="342d2-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="342d2-149">**hrvalidateipmsubtree**は、常に、ストアのルートフォルダーおよび [削除済みアイテム] フォルダー内の [ipm サブツリー] フォルダーに、検索ルートと ipm サブツリーのフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="342d2-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="342d2-150">[ipm Subtree] サブツリーフォルダーは、そのメッセージストア内の ipm 階層のルートです。</span><span class="sxs-lookup"><span data-stu-id="342d2-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="342d2-151">検索ルートフォルダーは、検索結果フォルダーのサブツリーのルートとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="342d2-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="342d2-152">ipm クライアントは、ipm サブツリーのルートフォルダーからフォルダー表示を表示し、その下に子フォルダーを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="342d2-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="342d2-153">メッセージストアのルートフォルダー内の情報は、クライアントのユーザーインターフェイスに表示されません。</span><span class="sxs-lookup"><span data-stu-id="342d2-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="342d2-154">この機能は、クライアントが情報を非表示にする必要がある場合に、その情報を IPM サブツリーのルートディレクトリに配置して、ユーザーには表示されないようにすることを意味します。</span><span class="sxs-lookup"><span data-stu-id="342d2-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="342d2-155">これに対して、サーバーベースのメッセージストアなど、メッセージやフォルダーをユーザーに対して非表示にする必要がある ipm 以外のアプリケーションは、それらを ipm 階層の外に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="342d2-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="342d2-156">**hrvalidateipmsubtree**は、作成する各 IPM フォルダーに有効なエントリ識別子があるかどうかを示す**PR_VALID_FOLDER_MASK**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="342d2-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="342d2-157">メッセージストアの次のエントリ識別子のプロパティは、対応するフォルダーのエントリ識別子に設定され、 **PR_VALID_FOLDER_MASK**と共に_lppprops_パラメーターで返されます。</span><span class="sxs-lookup"><span data-stu-id="342d2-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="342d2-158">**PR_COMMON_VIEWS_ENTRYID**([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="342d2-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="342d2-159">**PR_FINDER_ENTRYID**([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="342d2-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="342d2-160">**PR_IPM_OUTBOX_ENTRYID**([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="342d2-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="342d2-161">**PR_IPM_SENTMAIL_ENTRYID**([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="342d2-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="342d2-162">**PR_IPM_SUBTREE_ENTRYID**([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="342d2-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="342d2-163">**PR_IPM_WASTEBASKET_ENTRYID**([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="342d2-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="342d2-164">**PR_VIEWS_ENTRYID**([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="342d2-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="342d2-165">IPM 受信トレイのプレースホルダー [PROP_TAG](prop_tag.md) (PT_BINARY、PROP_ID_NULL)。</span><span class="sxs-lookup"><span data-stu-id="342d2-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="342d2-166">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="342d2-166">MFCMAPI reference</span></span>

<span data-ttu-id="342d2-167">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="342d2-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="342d2-168">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="342d2-168">**File**</span></span>|<span data-ttu-id="342d2-169">**関数**</span><span class="sxs-lookup"><span data-stu-id="342d2-169">**Function**</span></span>|<span data-ttu-id="342d2-170">**コメント**</span><span class="sxs-lookup"><span data-stu-id="342d2-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="342d2-171">MstStoreDlg</span><span class="sxs-lookup"><span data-stu-id="342d2-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="342d2-172">CMsgStoreDlg:: onvalidateipmsubtree</span><span class="sxs-lookup"><span data-stu-id="342d2-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="342d2-173">mfcmapi は、 **hrvalidateipmsubtree**メソッドを使用して、メッセージストアに標準フォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="342d2-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="342d2-174">関連項目</span><span class="sxs-lookup"><span data-stu-id="342d2-174">See also</span></span>



[<span data-ttu-id="342d2-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="342d2-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


<span data-ttu-id="342d2-176">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="342d2-176">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

