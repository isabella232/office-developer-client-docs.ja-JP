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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2625b148d15c2f5ccf65eedf3a1b1f2c9d0d133e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592046"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="40e10-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="40e10-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="40e10-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40e10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40e10-105">メッセージ ・ ストアには、標準的な個人間メッセージ (IPM) のフォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="40e10-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40e10-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="40e10-106">Header file:</span></span>  <br/> |<span data-ttu-id="40e10-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="40e10-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="40e10-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="40e10-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="40e10-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="40e10-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="40e10-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="40e10-110">Called by:</span></span>  <br/> |<span data-ttu-id="40e10-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="40e10-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="40e10-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="40e10-112">Parameters</span></span>

 <span data-ttu-id="40e10-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="40e10-113">_lpMDB_</span></span>
  
> <span data-ttu-id="40e10-114">[in]メッセージへのポインターでは、フォルダーを追加するオブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="40e10-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="40e10-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="40e10-115">_ulFlags_</span></span>
  
> <span data-ttu-id="40e10-116">[in]フォルダーを作成する方法を制御するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="40e10-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="40e10-117">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="40e10-117">The following flags can be set:</span></span>
    
<span data-ttu-id="40e10-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="40e10-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="40e10-119">フォルダーは、メッセージ ・ ストア ・ プロパティの指定が有効である場合でも、作成する前に確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40e10-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="40e10-120">エラーは、既存のフォルダー構造が破損していることを示す場合、クライアント アプリケーションは通常このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="40e10-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="40e10-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="40e10-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="40e10-122">IPM フォルダーの完全なセットは、メッセージ ストアのルート フォルダーに作成してください。</span><span class="sxs-lookup"><span data-stu-id="40e10-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="40e10-123">階層内のフォルダーのタイトルは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="40e10-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="40e10-124">フォルダー ビュー</span><span class="sxs-lookup"><span data-stu-id="40e10-124">Folder Views</span></span>
    
    - <span data-ttu-id="40e10-125">共通ビュー</span><span class="sxs-lookup"><span data-stu-id="40e10-125">Common Views</span></span>
    
    - <span data-ttu-id="40e10-126">ルートを検索します。\*</span><span class="sxs-lookup"><span data-stu-id="40e10-126">Search Root\*</span></span>
    
    - <span data-ttu-id="40e10-127">IPM サブツリー\*</span><span class="sxs-lookup"><span data-stu-id="40e10-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="40e10-128">受信トレイ</span><span class="sxs-lookup"><span data-stu-id="40e10-128">Inbox</span></span>
    
    - <span data-ttu-id="40e10-129">送信トレイ</span><span class="sxs-lookup"><span data-stu-id="40e10-129">Outbox</span></span>
    
    - <span data-ttu-id="40e10-130">削除済みアイテム\*</span><span class="sxs-lookup"><span data-stu-id="40e10-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="40e10-131">送信済みアイテム</span><span class="sxs-lookup"><span data-stu-id="40e10-131">Sent Items</span></span>
    
    <span data-ttu-id="40e10-132">3 つのフォルダーが付いて\*MAPI_FULL_IPM_TREE フラグが設定されていない場合でも作成される最小のセットです。</span><span class="sxs-lookup"><span data-stu-id="40e10-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="40e10-133">クライアント アプリケーションは、既定のストアでは、メッセージ ストアのフォルダーが作成されるときに通常このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="40e10-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="40e10-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="40e10-134">_lpcValues_</span></span>
  
> <span data-ttu-id="40e10-135">[で [チェック アウト]_LppProps_パラメーターで返される配列内の[SPropValue](spropvalue.md)構造体の数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="40e10-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="40e10-136">_LppProps_が NULL の場合、 _lpcValues_パラメーターの値は 0 にすることができます。</span><span class="sxs-lookup"><span data-stu-id="40e10-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="40e10-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="40e10-137">_lppProps_</span></span>
  
> <span data-ttu-id="40e10-138">[で [チェック アウト]**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) は、適切なフォルダーのエントリの識別子のプロパティのプロパティ値を含む**SPropValue**構造体の配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="40e10-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="40e10-139">**SPropValue**配列にはとしてコード化されたプロパティの特殊なタグで [受信トレイ] のエントリ id が含まれて**HrValidateIPMSubtree**は、メッセージ ・ ストアの受信トレイを作成する場合`PROP_TAG(PT_BINARY, PROP_ID_NULL)`。</span><span class="sxs-lookup"><span data-stu-id="40e10-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="40e10-140">_LppProps_のパラメーターには、呼び出し元の実装を**SPropValue**配列が返されることをする必要がないことを示す、NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="40e10-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="40e10-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="40e10-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="40e10-142">[out]エラーが発生するバージョン、コンポーネント、およびコンテキストの情報を格納する[MAPIERROR](mapierror.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="40e10-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="40e10-143">**MAPIERROR**構造体が返されない場合、 _lppMAPIError_パラメーターは NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="40e10-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="40e10-144">Return value</span><span class="sxs-lookup"><span data-stu-id="40e10-144">Return value</span></span>

<span data-ttu-id="40e10-145">なし。</span><span class="sxs-lookup"><span data-stu-id="40e10-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40e10-146">注釈</span><span class="sxs-lookup"><span data-stu-id="40e10-146">Remarks</span></span>

<span data-ttu-id="40e10-147">MAPI は、ストアを最初に開いたとき、またはストアが既定の保存を行った場合、メッセージ ストア内の標準の IPM サブツリーを作成するのには内部的に**HrValidateIPMSubtree**関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="40e10-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="40e10-148">この関数は、標準的なメッセージのフォルダーを修復または検証するクライアント アプリケーションによっても使用できます。</span><span class="sxs-lookup"><span data-stu-id="40e10-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="40e10-149">**HrValidateIPMSubtree**は常に、ストアのルート フォルダーと IPM サブツリー フォルダー内の削除済みアイテム フォルダーのルートを検索し、IPM サブツリー フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="40e10-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="40e10-150">IPM サブツリー フォルダーは、そのメッセージ ・ ストアに IPM の階層のルートです。</span><span class="sxs-lookup"><span data-stu-id="40e10-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="40e10-151">検索のルート フォルダーは、検索結果フォルダーのサブツリーのルートとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="40e10-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="40e10-152">IPM のクライアントでは、IPM サブツリーのルート フォルダーから開始し、子の下にあるフォルダーを表示、フォルダーのビューを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40e10-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="40e10-153">メッセージ ストアのルート フォルダー内の情報は、クライアントのユーザー インターフェイスに表示されません。</span><span class="sxs-lookup"><span data-stu-id="40e10-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="40e10-154">この機能は、クライアントには、情報が非表示にする必要がありますと、情報ことができますが配置される IPM サブツリーのルート ディレクトリに、ユーザーに表示されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="40e10-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="40e10-155">一方、IPM 以外のアプリケーション、サーバー ベースのメッセージ ・ ストアでは、ユーザーに表示するには、メッセージおよびフォルダーを必要とするまとめることができます IPM 階層に含まれない。</span><span class="sxs-lookup"><span data-stu-id="40e10-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="40e10-156">**HrValidateIPMSubtree**は、各 IPM フォルダーの作成が有効なエントリの識別子を持つかどうかを示すために**PR_VALID_FOLDER_MASK**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="40e10-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="40e10-157">メッセージ ・ ストアの次のエントリの識別子プロパティは対応するフォルダーのエントリ id を設定し、 **PR_VALID_FOLDER_MASK**および_lppProps_パラメーターに返されます。</span><span class="sxs-lookup"><span data-stu-id="40e10-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="40e10-158">**PR_COMMON_VIEWS_ENTRYID**([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40e10-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="40e10-159">**PR_FINDER_ENTRYID**([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40e10-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="40e10-160">**PR_IPM_OUTBOX_ENTRYID**([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40e10-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="40e10-161">**PR_IPM_SENTMAIL_ENTRYID**([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40e10-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="40e10-162">**PR_IPM_SUBTREE_ENTRYID**([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40e10-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="40e10-163">**PR_IPM_WASTEBASKET_ENTRYID**([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40e10-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="40e10-164">**PR_VIEWS_ENTRYID**([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="40e10-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="40e10-165">プレース ホルダー (PT_BINARY, PROP_ID_NULL)、IPM の受信トレイに[PROP_TAG](prop_tag.md) 。</span><span class="sxs-lookup"><span data-stu-id="40e10-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="40e10-166">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="40e10-166">MFCMAPI reference</span></span>

<span data-ttu-id="40e10-167">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="40e10-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="40e10-168">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="40e10-168">**File**</span></span>|<span data-ttu-id="40e10-169">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="40e10-169">**Function**</span></span>|<span data-ttu-id="40e10-170">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="40e10-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="40e10-171">MstStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="40e10-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="40e10-172">CMsgStoreDlg::OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="40e10-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="40e10-173">MFCMAPI では、 **HrValidateIPMSubtree**メソッドを使用して、メッセージ ・ ストアに標準的なフォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="40e10-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40e10-174">関連項目</span><span class="sxs-lookup"><span data-stu-id="40e10-174">See also</span></span>



[<span data-ttu-id="40e10-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="40e10-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


<span data-ttu-id="40e10-176">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="40e10-176">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

