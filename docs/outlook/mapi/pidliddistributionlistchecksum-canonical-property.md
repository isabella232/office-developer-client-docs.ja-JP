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
ms.openlocfilehash: 44752e147569619589b23a380b2fefa511724ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571732"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a><span data-ttu-id="f01a8-103">PidLidDistributionListChecksum 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f01a8-103">PidLidDistributionListChecksum Canonical Property</span></span>

  
  
<span data-ttu-id="f01a8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f01a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f01a8-105">32 ビット巡回冗長チェック (CRC 32) 多項式のチェックサムを個人用配布リストを指定します。</span><span class="sxs-lookup"><span data-stu-id="f01a8-105">Specifies the 32-bit cyclic redundancy check (CRC-32) polynomial checksum for a personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f01a8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f01a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f01a8-107">dispidDLChecksum</span><span class="sxs-lookup"><span data-stu-id="f01a8-107">dispidDLChecksum</span></span>  <br/> |
|<span data-ttu-id="f01a8-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f01a8-108">Property set:</span></span>  <br/> |<span data-ttu-id="f01a8-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="f01a8-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="f01a8-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f01a8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f01a8-111">0x0000804C</span><span class="sxs-lookup"><span data-stu-id="f01a8-111">0x0000804C</span></span>  <br/> |
|<span data-ttu-id="f01a8-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f01a8-112">Data type:</span></span>  <br/> |<span data-ttu-id="f01a8-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f01a8-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f01a8-114">領域:</span><span class="sxs-lookup"><span data-stu-id="f01a8-114">Area:</span></span>  <br/> |<span data-ttu-id="f01a8-115">Contact</span><span class="sxs-lookup"><span data-stu-id="f01a8-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f01a8-116">注釈</span><span class="sxs-lookup"><span data-stu-id="f01a8-116">Remarks</span></span>

<span data-ttu-id="f01a8-117">既存の crc-32 を計算することによって、他の個人用配布リスト メンバーのプロパティを更新せずに、 **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) のプロパティが更新されたときを検出するためにこのプロパティの値を使用することができます。**dispidDLMembers**および**dispidDLChecksum**プロパティの値と比較することの値です。</span><span class="sxs-lookup"><span data-stu-id="f01a8-117">The value of this property can be used to detect when the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property was updated without updating the other personal distribution list member properties by computing the CRC-32 on the existing value of **dispidDLMembers** and comparing it with the value of the **dispidDLChecksum** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f01a8-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f01a8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f01a8-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f01a8-119">Protocol specifications</span></span>

<span data-ttu-id="f01a8-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f01a8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f01a8-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f01a8-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f01a8-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f01a8-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f01a8-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f01a8-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f01a8-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f01a8-124">Header files</span></span>

<span data-ttu-id="f01a8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f01a8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f01a8-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f01a8-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f01a8-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="f01a8-127">See also</span></span>



[<span data-ttu-id="f01a8-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f01a8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f01a8-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f01a8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f01a8-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f01a8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f01a8-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f01a8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

