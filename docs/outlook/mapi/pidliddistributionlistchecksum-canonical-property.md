---
title: PidLidDistributionListChecksum 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidDistributionListChecksum
api_type:
- COM
ms.assetid: bd50ab34-caae-4258-8afc-769e3cbc5220
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ac1f0d839b1ea059ec2b8d94556808bea3850862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357611"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a><span data-ttu-id="07ddb-103">PidLidDistributionListChecksum 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="07ddb-103">PidLidDistributionListChecksum Canonical Property</span></span>

  
  
<span data-ttu-id="07ddb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07ddb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07ddb-105">個人用配布リストの32ビット巡回冗長チェック (CRC-32) 多項式チェックサムを指定します。</span><span class="sxs-lookup"><span data-stu-id="07ddb-105">Specifies the 32-bit cyclic redundancy check (CRC-32) polynomial checksum for a personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07ddb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="07ddb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07ddb-107">dispiddlchecksum</span><span class="sxs-lookup"><span data-stu-id="07ddb-107">dispidDLChecksum</span></span>  <br/> |
|<span data-ttu-id="07ddb-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="07ddb-108">Property set:</span></span>  <br/> |<span data-ttu-id="07ddb-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="07ddb-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="07ddb-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="07ddb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="07ddb-111">0x0000804c</span><span class="sxs-lookup"><span data-stu-id="07ddb-111">0x0000804C</span></span>  <br/> |
|<span data-ttu-id="07ddb-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="07ddb-112">Data type:</span></span>  <br/> |<span data-ttu-id="07ddb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="07ddb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="07ddb-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="07ddb-114">Area:</span></span>  <br/> |<span data-ttu-id="07ddb-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="07ddb-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07ddb-116">解説</span><span class="sxs-lookup"><span data-stu-id="07ddb-116">Remarks</span></span>

<span data-ttu-id="07ddb-117">このプロパティの値は、既存のを使用して32を計算することによって、他の個人用配布リストのメンバープロパティを更新せずに、 **dispiddlmembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) プロパティを更新したときに検出することができます。dispiddlmembers**メンバー**の値と、 **dispiddlmembers**プロパティの値との比較。</span><span class="sxs-lookup"><span data-stu-id="07ddb-117">The value of this property can be used to detect when the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property was updated without updating the other personal distribution list member properties by computing the CRC-32 on the existing value of **dispidDLMembers** and comparing it with the value of the **dispidDLChecksum** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="07ddb-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="07ddb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="07ddb-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="07ddb-119">Protocol specifications</span></span>

<span data-ttu-id="07ddb-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07ddb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07ddb-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="07ddb-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="07ddb-122">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07ddb-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07ddb-123">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="07ddb-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="07ddb-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="07ddb-124">Header files</span></span>

<span data-ttu-id="07ddb-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07ddb-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="07ddb-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="07ddb-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07ddb-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="07ddb-127">See also</span></span>



[<span data-ttu-id="07ddb-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="07ddb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07ddb-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="07ddb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07ddb-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="07ddb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07ddb-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="07ddb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

