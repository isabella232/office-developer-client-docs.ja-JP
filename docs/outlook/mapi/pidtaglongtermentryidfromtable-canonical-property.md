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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 574c7d305f105709aebcd41e30b034fbac1892a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425667"
---
# <a name="pidtaglongtermentryidfromtable-canonical-property"></a><span data-ttu-id="18619-103">PidTagLongTermEntryIdFromTable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="18619-103">PidTagLongTermEntryIdFromTable Canonical Property</span></span>

  
  
<span data-ttu-id="18619-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18619-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18619-105">アイテムの長期エントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="18619-105">Obtains the long- term entry identifier of an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18619-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="18619-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18619-107">PR_LONGTERM_ENTRYID_FROM_TABLE</span><span class="sxs-lookup"><span data-stu-id="18619-107">PR_LONGTERM_ENTRYID_FROM_TABLE</span></span>  <br/> |
|<span data-ttu-id="18619-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="18619-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18619-109">0x6670</span><span class="sxs-lookup"><span data-stu-id="18619-109">0x6670</span></span>  <br/> |
|<span data-ttu-id="18619-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="18619-110">Data type:</span></span>  <br/> |<span data-ttu-id="18619-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="18619-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="18619-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="18619-112">Area:</span></span>  <br/> |<span data-ttu-id="18619-113">Table プロパティ</span><span class="sxs-lookup"><span data-stu-id="18619-113">Table Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18619-114">注釈</span><span class="sxs-lookup"><span data-stu-id="18619-114">Remarks</span></span>

<span data-ttu-id="18619-115">このプロパティは、コンテンツ テーブルで使用して、短期的なエントリ識別子の代わりに、アイテムのエントリ識別子を長期エントリ識別子として取得できます。</span><span class="sxs-lookup"><span data-stu-id="18619-115">This property can be used in a contents table to get the entry identifier of an item as a long-term entry identifier instead of a short-term entry identifier.</span></span> <span data-ttu-id="18619-116">長期識別子と短期識別子の詳細については、「PR_ENTRYID **(** [PidTagEntryId)」を参照してください](pidtagentryid-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="18619-116">For information about long-term and short-term identifiers, see **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18619-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="18619-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="18619-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="18619-118">Header files</span></span>

<span data-ttu-id="18619-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18619-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="18619-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="18619-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="18619-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="18619-121">Mapitags.h</span></span>
  
> <span data-ttu-id="18619-122">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="18619-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18619-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="18619-123">See also</span></span>



[<span data-ttu-id="18619-124">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="18619-124">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="18619-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="18619-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18619-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="18619-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18619-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="18619-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18619-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="18619-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

