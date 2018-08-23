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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ae09723c78fe4e333fb5c46e8c79da4b77c0b331
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803666"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="725f9-103">PidTagValidFolderMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="725f9-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="725f9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="725f9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="725f9-105">メッセージ ストア内のフォルダーのエントリ id の有効性を示すフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="725f9-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="725f9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="725f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="725f9-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="725f9-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="725f9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="725f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="725f9-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="725f9-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="725f9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="725f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="725f9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="725f9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="725f9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="725f9-112">Area:</span></span>  <br/> |<span data-ttu-id="725f9-113">MAPI メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="725f9-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="725f9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="725f9-114">Remarks</span></span>

<span data-ttu-id="725f9-115">メッセージ ストアが破損した場合や、ユーザーがフォルダーを削除した場合フォルダーのエントリ id が無効になることができます。</span><span class="sxs-lookup"><span data-stu-id="725f9-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="725f9-116">1 つ以上次のフラグのビットマスクを設定できます。</span><span class="sxs-lookup"><span data-stu-id="725f9-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="725f9-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="725f9-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="725f9-118">共通ビュー] フォルダーには、有効なエントリの識別子があります。</span><span class="sxs-lookup"><span data-stu-id="725f9-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="725f9-119">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="725f9-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="725f9-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="725f9-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="725f9-121">Finder フォルダーには、有効なエントリの識別子があります。</span><span class="sxs-lookup"><span data-stu-id="725f9-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="725f9-122">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="725f9-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="725f9-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="725f9-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="725f9-124">個人間メッセージ (IPM) が表示されるフォルダーには、エントリの有効な識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="725f9-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="725f9-125">[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="725f9-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="725f9-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="725f9-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="725f9-127">IPM が送信トレイ フォルダーには、有効なエントリの識別子があります。</span><span class="sxs-lookup"><span data-stu-id="725f9-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="725f9-128">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="725f9-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="725f9-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="725f9-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="725f9-130">IPM の送信済みアイテム フォルダーには、有効なエントリの識別子があります。</span><span class="sxs-lookup"><span data-stu-id="725f9-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="725f9-131">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="725f9-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="725f9-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="725f9-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="725f9-133">IPM フォルダーのサブツリーには、有効なエントリの識別子があります。</span><span class="sxs-lookup"><span data-stu-id="725f9-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="725f9-134">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="725f9-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="725f9-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="725f9-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="725f9-136">IPM の削除済みアイテム フォルダーには、有効なエントリの識別子があります。</span><span class="sxs-lookup"><span data-stu-id="725f9-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="725f9-137">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="725f9-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="725f9-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="725f9-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="725f9-139">Views フォルダーには、有効なエントリの識別子があります。</span><span class="sxs-lookup"><span data-stu-id="725f9-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="725f9-140">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="725f9-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="725f9-141">関連リソース</span><span class="sxs-lookup"><span data-stu-id="725f9-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="725f9-142">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="725f9-142">Header files</span></span>

<span data-ttu-id="725f9-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="725f9-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="725f9-144">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="725f9-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="725f9-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="725f9-145">Mapitags.h</span></span>
  
> <span data-ttu-id="725f9-146">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="725f9-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="725f9-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="725f9-147">See also</span></span>



[<span data-ttu-id="725f9-148">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="725f9-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="725f9-149">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="725f9-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="725f9-150">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="725f9-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="725f9-151">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="725f9-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

