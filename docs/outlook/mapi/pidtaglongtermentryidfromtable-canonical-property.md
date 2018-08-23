---
title: PidTagLongTermEntryIdFromTable 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLongTermEntryIdFromTable
api_type:
- HeaderDef
ms.assetid: d9457fea-4b1e-4cf6-9c4b-14c98fbec2a1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ddec060af73d61a4a39c59b35f0442d6b9b1db66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590317"
---
# <a name="pidtaglongtermentryidfromtable-canonical-property"></a><span data-ttu-id="06993-103">PidTagLongTermEntryIdFromTable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="06993-103">PidTagLongTermEntryIdFromTable Canonical Property</span></span>

  
  
<span data-ttu-id="06993-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06993-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06993-105">アイテムの長期間のエントリの識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="06993-105">Obtains the long- term entry identifier of an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06993-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="06993-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06993-107">PR_LONGTERM_ENTRYID_FROM_TABLE</span><span class="sxs-lookup"><span data-stu-id="06993-107">PR_LONGTERM_ENTRYID_FROM_TABLE</span></span>  <br/> |
|<span data-ttu-id="06993-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="06993-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06993-109">0x6670</span><span class="sxs-lookup"><span data-stu-id="06993-109">0x6670</span></span>  <br/> |
|<span data-ttu-id="06993-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="06993-110">Data type:</span></span>  <br/> |<span data-ttu-id="06993-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="06993-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="06993-112">領域:</span><span class="sxs-lookup"><span data-stu-id="06993-112">Area:</span></span>  <br/> |<span data-ttu-id="06993-113">テーブルのプロパティ</span><span class="sxs-lookup"><span data-stu-id="06993-113">Table Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06993-114">注釈</span><span class="sxs-lookup"><span data-stu-id="06993-114">Remarks</span></span>

<span data-ttu-id="06993-115">このプロパティは、短期的なエントリの識別子ではなく、長期的なエントリ id と、アイテムのエントリ id を取得するのには内容のテーブルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="06993-115">This property can be used in a contents table to get the entry identifier of an item as a long-term entry identifier instead of a short-term entry identifier.</span></span> <span data-ttu-id="06993-116">長期的および短期的な識別子の詳細については、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06993-116">For information about long-term and short-term identifiers, see **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="06993-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="06993-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="06993-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="06993-118">Header files</span></span>

<span data-ttu-id="06993-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06993-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="06993-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="06993-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="06993-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06993-121">Mapitags.h</span></span>
  
> <span data-ttu-id="06993-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06993-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06993-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="06993-123">See also</span></span>



[<span data-ttu-id="06993-124">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="06993-124">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="06993-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="06993-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06993-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="06993-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06993-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="06993-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06993-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="06993-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

