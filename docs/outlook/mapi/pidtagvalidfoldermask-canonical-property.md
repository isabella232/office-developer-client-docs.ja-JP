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
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="9a3bd-103">PidTagValidFolderMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9a3bd-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="9a3bd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a3bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a3bd-105">メッセージストア内のフォルダーのエントリ識別子の有効性を示すフラグのビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9a3bd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9a3bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9a3bd-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="9a3bd-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="9a3bd-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9a3bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9a3bd-109">0x35df</span><span class="sxs-lookup"><span data-stu-id="9a3bd-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="9a3bd-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9a3bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="9a3bd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9a3bd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9a3bd-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9a3bd-112">Area:</span></span>  <br/> |<span data-ttu-id="9a3bd-113">MAPI メッセージストア</span><span class="sxs-lookup"><span data-stu-id="9a3bd-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a3bd-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9a3bd-114">Remarks</span></span>

<span data-ttu-id="9a3bd-115">ユーザーがフォルダーを削除したり、メッセージストアが破損したりすると、フォルダーのエントリ識別子が無効になることがあります。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="9a3bd-116">ビットマスクには、次の1つ以上のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="9a3bd-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="9a3bd-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="9a3bd-118">common views フォルダーには、有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="9a3bd-119">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="9a3bd-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="9a3bd-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="9a3bd-121">finder フォルダーには有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="9a3bd-122">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="9a3bd-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="9a3bd-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="9a3bd-124">個人間メッセージ (IPM) の受信フォルダーに有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="9a3bd-125">[IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="9a3bd-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="9a3bd-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="9a3bd-127">IPM 送信トレイフォルダーに有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="9a3bd-128">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="9a3bd-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="9a3bd-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="9a3bd-130">IPM 送信済みアイテムフォルダーには、有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="9a3bd-131">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="9a3bd-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="9a3bd-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="9a3bd-133">IPM フォルダーのサブツリーに有効なエントリ識別子がある。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="9a3bd-134">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="9a3bd-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="9a3bd-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="9a3bd-136">IPM 削除済みアイテムフォルダーには、有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="9a3bd-137">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="9a3bd-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="9a3bd-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="9a3bd-139">views フォルダーには有効なエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="9a3bd-140">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="9a3bd-141">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9a3bd-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9a3bd-142">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9a3bd-142">Header files</span></span>

<span data-ttu-id="9a3bd-143">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9a3bd-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="9a3bd-144">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="9a3bd-145">Mapitags</span><span class="sxs-lookup"><span data-stu-id="9a3bd-145">Mapitags.h</span></span>
  
> <span data-ttu-id="9a3bd-146">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9a3bd-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9a3bd-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="9a3bd-147">See also</span></span>



[<span data-ttu-id="9a3bd-148">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9a3bd-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9a3bd-149">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9a3bd-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9a3bd-150">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9a3bd-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9a3bd-151">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9a3bd-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

