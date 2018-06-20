---
title: PidTagLongTermEntryIdFromTable の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ebb925ac1ff6507a5e686b769ba9d48b095fb527
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802963"
---
# <a name="pidtaglongtermentryidfromtable-canonical-property"></a><span data-ttu-id="366d9-103">PidTagLongTermEntryIdFromTable の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="366d9-103">PidTagLongTermEntryIdFromTable Canonical Property</span></span>

  
  
<span data-ttu-id="366d9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="366d9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="366d9-105">アイテムの長期間のエントリの識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="366d9-105">Obtains the long- term entry identifier of an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="366d9-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="366d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="366d9-107">PR_LONGTERM_ENTRYID_FROM_TABLE</span><span class="sxs-lookup"><span data-stu-id="366d9-107">PR_LONGTERM_ENTRYID_FROM_TABLE</span></span>  <br/> |
|<span data-ttu-id="366d9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="366d9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="366d9-109">0x6670</span><span class="sxs-lookup"><span data-stu-id="366d9-109">0x6670</span></span>  <br/> |
|<span data-ttu-id="366d9-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="366d9-110">Data type:</span></span>  <br/> |<span data-ttu-id="366d9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="366d9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="366d9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="366d9-112">Area:</span></span>  <br/> |<span data-ttu-id="366d9-113">テーブルのプロパティ</span><span class="sxs-lookup"><span data-stu-id="366d9-113">Table Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="366d9-114">備考</span><span class="sxs-lookup"><span data-stu-id="366d9-114">Remarks</span></span>

<span data-ttu-id="366d9-115">このプロパティは、短期的なエントリの識別子ではなく、長期的なエントリ id と、アイテムのエントリ id を取得するのには内容のテーブルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="366d9-115">This property can be used in a contents table to get the entry identifier of an item as a long-term entry identifier instead of a short-term entry identifier.</span></span> <span data-ttu-id="366d9-116">長期的および短期的な識別子の詳細については、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="366d9-116">For information about long-term and short-term identifiers, see **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="366d9-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="366d9-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="366d9-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="366d9-118">Header files</span></span>

<span data-ttu-id="366d9-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="366d9-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="366d9-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="366d9-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="366d9-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="366d9-121">Mapitags.h</span></span>
  
> <span data-ttu-id="366d9-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="366d9-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="366d9-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="366d9-123">See also</span></span>



[<span data-ttu-id="366d9-124">PidTagEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="366d9-124">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="366d9-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="366d9-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="366d9-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="366d9-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="366d9-127">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="366d9-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="366d9-128">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="366d9-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

