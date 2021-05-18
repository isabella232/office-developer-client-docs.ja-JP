---
title: PidTagExtendedRuleSizeLimit 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 347d84021b7e9ece925acb99e8b539ba608337a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316346"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a><span data-ttu-id="84cf5-103">PidTagExtendedRuleSizeLimit 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="84cf5-103">PidTagExtendedRuleSizeLimit Canonical Property</span></span>

  
  
<span data-ttu-id="84cf5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84cf5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84cf5-105">ユーザーが単一の "拡張" ルールに対して累積できる最大サイズをバイト単位で格納します。</span><span class="sxs-lookup"><span data-stu-id="84cf5-105">Contains the maximum size, in bytes, the user is allowed to accumulate for a single "extended" rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84cf5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="84cf5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84cf5-107">PR_EXTENDED_RULE_SIZE_LIMIT</span><span class="sxs-lookup"><span data-stu-id="84cf5-107">PR_EXTENDED_RULE_SIZE_LIMIT</span></span>  <br/> |
|<span data-ttu-id="84cf5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="84cf5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84cf5-109">0x0E9B</span><span class="sxs-lookup"><span data-stu-id="84cf5-109">0x0E9B</span></span>  <br/> |
|<span data-ttu-id="84cf5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="84cf5-110">Data type:</span></span>  <br/> |<span data-ttu-id="84cf5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="84cf5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="84cf5-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="84cf5-112">Area:</span></span>  <br/> |<span data-ttu-id="84cf5-113">ルール</span><span class="sxs-lookup"><span data-stu-id="84cf5-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84cf5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="84cf5-114">Remarks</span></span>

<span data-ttu-id="84cf5-115">このプロパティがログオン オブジェクトに設定されている場合、クライアントは **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) プロパティのサイズをこのプロパティで指定された値の下に保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84cf5-115">If this property is set on the logon object, the client should keep the size of the **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) property under the value specified by this property.</span></span> <span data-ttu-id="84cf5-116">逆に、クライアントが大きすぎるバイナリ プロパティを設定しようとすると、サーバーはエラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="84cf5-116">Conversely, the server should return an error if the client does attempt to set a binary property that is too large.</span></span>
  
<span data-ttu-id="84cf5-117">拡張ルールの詳細については [、「[MS-OXORULE]」を参照してください](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="84cf5-117">For information about extended rules, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="84cf5-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="84cf5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84cf5-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="84cf5-119">Protocol specifications</span></span>

<span data-ttu-id="84cf5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84cf5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84cf5-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="84cf5-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84cf5-122">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84cf5-122">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84cf5-123">コア メッセージ ストア オブジェクトに対して許容される操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="84cf5-123">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84cf5-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="84cf5-124">Header files</span></span>

<span data-ttu-id="84cf5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84cf5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="84cf5-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="84cf5-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="84cf5-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="84cf5-127">Mapitags.h</span></span>
  
> <span data-ttu-id="84cf5-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="84cf5-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84cf5-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="84cf5-129">See also</span></span>



[<span data-ttu-id="84cf5-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="84cf5-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84cf5-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="84cf5-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84cf5-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="84cf5-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84cf5-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="84cf5-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

