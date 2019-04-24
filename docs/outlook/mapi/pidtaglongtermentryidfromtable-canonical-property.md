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
ms.openlocfilehash: 574c7d305f105709aebcd41e30b034fbac1892a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278779"
---
# <a name="pidtaglongtermentryidfromtable-canonical-property"></a><span data-ttu-id="155c0-103">PidTagLongTermEntryIdFromTable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="155c0-103">PidTagLongTermEntryIdFromTable Canonical Property</span></span>

  
  
<span data-ttu-id="155c0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="155c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="155c0-105">アイテムの長期のエントリ id を取得します。</span><span class="sxs-lookup"><span data-stu-id="155c0-105">Obtains the long- term entry identifier of an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="155c0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="155c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="155c0-107">PR_LONGTERM_ENTRYID_FROM_TABLE</span><span class="sxs-lookup"><span data-stu-id="155c0-107">PR_LONGTERM_ENTRYID_FROM_TABLE</span></span>  <br/> |
|<span data-ttu-id="155c0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="155c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="155c0-109">0x6670</span><span class="sxs-lookup"><span data-stu-id="155c0-109">0x6670</span></span>  <br/> |
|<span data-ttu-id="155c0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="155c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="155c0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="155c0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="155c0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="155c0-112">Area:</span></span>  <br/> |<span data-ttu-id="155c0-113">表のプロパティ</span><span class="sxs-lookup"><span data-stu-id="155c0-113">Table Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="155c0-114">解説</span><span class="sxs-lookup"><span data-stu-id="155c0-114">Remarks</span></span>

<span data-ttu-id="155c0-115">このプロパティは、アイテムのエントリ識別子を短い用語のエントリ id ではなく、長期間のエントリ id として取得するために、contents テーブルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="155c0-115">This property can be used in a contents table to get the entry identifier of an item as a long-term entry identifier instead of a short-term entry identifier.</span></span> <span data-ttu-id="155c0-116">長期および短期の識別子については、「 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="155c0-116">For information about long-term and short-term identifiers, see **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="155c0-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="155c0-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="155c0-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="155c0-118">Header files</span></span>

<span data-ttu-id="155c0-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="155c0-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="155c0-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="155c0-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="155c0-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="155c0-121">Mapitags.h</span></span>
  
> <span data-ttu-id="155c0-122">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="155c0-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="155c0-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="155c0-123">See also</span></span>



[<span data-ttu-id="155c0-124">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="155c0-124">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="155c0-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="155c0-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="155c0-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="155c0-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="155c0-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="155c0-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="155c0-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="155c0-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

