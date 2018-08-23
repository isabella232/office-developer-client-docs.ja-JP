---
title: PidTagStoreRecordKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreRecordKey
api_type:
- COM
ms.assetid: 27347302-bd52-4f62-98f1-6c37f9a66463
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 08527f3325742eb7c48f11c2ed7d08f71fa3e972
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592711"
---
# <a name="pidtagstorerecordkey-canonical-property"></a><span data-ttu-id="76ad8-103">PidTagStoreRecordKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="76ad8-103">PidTagStoreRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="76ad8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76ad8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76ad8-105">バイナリ比較の一意の識別子 (キーのレコード) オブジェクトが格納されているメッセージ ストアが含まれています。</span><span class="sxs-lookup"><span data-stu-id="76ad8-105">Contains the unique binary-comparable identifier (record key) of the message store in which an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76ad8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="76ad8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76ad8-107">PR_STORE_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="76ad8-107">PR_STORE_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="76ad8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="76ad8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="76ad8-109">0x0FFA</span><span class="sxs-lookup"><span data-stu-id="76ad8-109">0x0FFA</span></span>  <br/> |
|<span data-ttu-id="76ad8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="76ad8-110">Data type:</span></span>  <br/> |<span data-ttu-id="76ad8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="76ad8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="76ad8-112">領域:</span><span class="sxs-lookup"><span data-stu-id="76ad8-112">Area:</span></span>  <br/> |<span data-ttu-id="76ad8-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="76ad8-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76ad8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="76ad8-114">Remarks</span></span>

<span data-ttu-id="76ad8-115">メッセージ ・ ストアのこのプロパティは、ストアの**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) のプロパティと同じです。</span><span class="sxs-lookup"><span data-stu-id="76ad8-115">For a message store, this property is identical to the store's own **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="76ad8-116">このプロパティと**PR_RECORD_KEY**間の関係は、 **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) と**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) との間の関係と同じです。</span><span class="sxs-lookup"><span data-stu-id="76ad8-116">The relationship between this property and **PR_RECORD_KEY** is the same as the relationship between **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="76ad8-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="76ad8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="76ad8-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="76ad8-118">Protocol specifications</span></span>

<span data-ttu-id="76ad8-119">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76ad8-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76ad8-120">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="76ad8-120">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="76ad8-121">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76ad8-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76ad8-122">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="76ad8-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="76ad8-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="76ad8-123">Header files</span></span>

<span data-ttu-id="76ad8-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76ad8-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="76ad8-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="76ad8-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="76ad8-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="76ad8-126">Mapitags.h</span></span>
  
> <span data-ttu-id="76ad8-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="76ad8-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76ad8-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="76ad8-128">See also</span></span>



[<span data-ttu-id="76ad8-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="76ad8-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76ad8-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="76ad8-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76ad8-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="76ad8-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76ad8-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="76ad8-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

