---
title: PidLidDistributionListName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListName
api_type:
- COM
ms.assetid: 06fe4d20-c3f5-4f4f-b7b7-5a4f5257079b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d3a1229f4d29bae36b90eb1daf0b6426f358b598
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341966"
---
# <a name="pidliddistributionlistname-canonical-property"></a><span data-ttu-id="e6918-103">PidLidDistributionListName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e6918-103">PidLidDistributionListName Canonical Property</span></span>

  
  
<span data-ttu-id="e6918-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6918-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6918-105">個人用配布リストの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e6918-105">Specifies the name of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6918-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e6918-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e6918-107">dispiddlname</span><span class="sxs-lookup"><span data-stu-id="e6918-107">dispidDLName</span></span>  <br/> |
|<span data-ttu-id="e6918-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="e6918-108">Property set:</span></span>  <br/> |<span data-ttu-id="e6918-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="e6918-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="e6918-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e6918-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e6918-111">0x00008053</span><span class="sxs-lookup"><span data-stu-id="e6918-111">0x00008053</span></span>  <br/> |
|<span data-ttu-id="e6918-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e6918-112">Data type:</span></span>  <br/> |<span data-ttu-id="e6918-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e6918-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e6918-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="e6918-114">Area:</span></span>  <br/> |<span data-ttu-id="e6918-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="e6918-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6918-116">解説</span><span class="sxs-lookup"><span data-stu-id="e6918-116">Remarks</span></span>

<span data-ttu-id="e6918-117">このプロパティの値は、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6918-117">The value of this property should be the same as the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e6918-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e6918-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e6918-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e6918-119">Protocol specifications</span></span>

<span data-ttu-id="e6918-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6918-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6918-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e6918-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e6918-122">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6918-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6918-123">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e6918-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e6918-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e6918-124">Header files</span></span>

<span data-ttu-id="e6918-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6918-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e6918-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e6918-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e6918-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e6918-127">See also</span></span>



[<span data-ttu-id="e6918-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e6918-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e6918-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e6918-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e6918-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e6918-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e6918-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e6918-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

