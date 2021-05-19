---
title: PidTagValidFolderMask 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 925e0eb60d55349ded114b827b6ca67e3b5ac1ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427795"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="2c376-103">PidTagValidFolderMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2c376-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="2c376-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c376-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c376-105">メッセージ ストア内のフォルダーのエントリ識別子の有効性を示すフラグのビットマスクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2c376-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c376-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2c376-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c376-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="2c376-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="2c376-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2c376-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c376-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="2c376-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="2c376-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2c376-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c376-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2c376-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2c376-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2c376-112">Area:</span></span>  <br/> |<span data-ttu-id="2c376-113">MAPI メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="2c376-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c376-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2c376-114">Remarks</span></span>

<span data-ttu-id="2c376-115">ユーザーがフォルダーを削除した場合、またはメッセージ ストアが破損した場合、フォルダーのエントリ識別子が無効になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2c376-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="2c376-116">ビットマスクには、次のフラグを 1 つ以上設定できます。</span><span class="sxs-lookup"><span data-stu-id="2c376-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="2c376-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="2c376-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="2c376-118">共通ビュー フォルダーには、有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="2c376-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="2c376-119">**「PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId)」を参照してください](pidtagcommonviewsentryid-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="2c376-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="2c376-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="2c376-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="2c376-121">finder フォルダーには、有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="2c376-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="2c376-122">詳細 **についてはPR_FINDER_ENTRYID** ([PidTagFinderEntryId ) を参照してください](pidtagfinderentryid-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="2c376-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="2c376-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="2c376-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="2c376-124">対人メッセージ (IPM) 受信フォルダーには、有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="2c376-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="2c376-125">[「IMsgStore::GetReceiveFolder」を参照してください](imsgstore-getreceivefolder.md)。</span><span class="sxs-lookup"><span data-stu-id="2c376-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="2c376-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="2c376-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="2c376-127">IPM 送信ボックス フォルダーには、有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="2c376-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="2c376-128">**「PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId)」を参照してください](pidtagipmoutboxentryid-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="2c376-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="2c376-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="2c376-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="2c376-130">IPM 送信アイテム フォルダーには、有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="2c376-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="2c376-131">**「PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId)」を参照してください](pidtagipmsentmailentryid-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="2c376-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="2c376-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="2c376-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="2c376-133">IPM フォルダー サブツリーには、有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="2c376-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="2c376-134">**「PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId)」を参照してください](pidtagipmsubtreeentryid-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="2c376-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="2c376-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="2c376-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="2c376-136">IPM 削除済みアイテム フォルダーには、有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="2c376-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="2c376-137">**「PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId)」を参照してください](pidtagipmwastebasketentryid-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="2c376-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="2c376-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="2c376-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="2c376-139">views フォルダーには、有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="2c376-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="2c376-140">詳細 **についてはPR_VIEWS_ENTRYID** ([PidTagViewsEntryId ) を参照してください](pidtagviewsentryid-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="2c376-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="2c376-141">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2c376-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2c376-142">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2c376-142">Header files</span></span>

<span data-ttu-id="2c376-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c376-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c376-144">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2c376-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c376-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2c376-145">Mapitags.h</span></span>
  
> <span data-ttu-id="2c376-146">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="2c376-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c376-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c376-147">See also</span></span>



[<span data-ttu-id="2c376-148">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2c376-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c376-149">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2c376-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c376-150">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2c376-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c376-151">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2c376-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

