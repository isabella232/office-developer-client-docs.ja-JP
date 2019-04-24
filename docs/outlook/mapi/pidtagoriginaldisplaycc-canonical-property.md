---
title: PidTagOriginalDisplayCc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayCc
api_type:
- COM
ms.assetid: f48d723c-3ad8-4617-952a-ba5216b2129c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9eb90d353705434803ff617ff2b355c7c96359b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355623"
---
# <a name="pidtagoriginaldisplaycc-canonical-property"></a><span data-ttu-id="d692a-103">PidTagOriginalDisplayCc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d692a-103">PidTagOriginalDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="d692a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d692a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d692a-105">元のメッセージのすべてのカーボンコピー (CC) 受信者の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d692a-105">Contains the display names of any carbon copy (CC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d692a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d692a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d692a-107">PR_ORIGINAL_DISPLAY_CC、PR_ORIGINAL_DISPLAY_CC_A、PR_ORIGINAL_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="d692a-107">PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="d692a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d692a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d692a-109">0x0073</span><span class="sxs-lookup"><span data-stu-id="d692a-109">0x0073</span></span>  <br/> |
|<span data-ttu-id="d692a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d692a-110">Data type:</span></span>  <br/> |<span data-ttu-id="d692a-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d692a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d692a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d692a-112">Area:</span></span>  <br/> |<span data-ttu-id="d692a-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="d692a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d692a-114">解説</span><span class="sxs-lookup"><span data-stu-id="d692a-114">Remarks</span></span>

<span data-ttu-id="d692a-115">これらのプロパティには、セミコロンで区切られたリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d692a-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="d692a-116">これは MAPI によって提供され、配信レポートまたは配信不能レポートまたは読み取りまたは非開封レポートが生成されたときに、 **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) から直接コピーされます。</span><span class="sxs-lookup"><span data-stu-id="d692a-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="d692a-117">このプロパティは、メッセージクラスによって定義されている他のメッセージに表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="d692a-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d692a-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d692a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d692a-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d692a-119">Protocol specifications</span></span>

<span data-ttu-id="d692a-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d692a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d692a-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d692a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d692a-122">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d692a-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d692a-123">電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d692a-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d692a-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="d692a-124">Header files</span></span>

<span data-ttu-id="d692a-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d692a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d692a-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d692a-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d692a-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="d692a-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d692a-128">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d692a-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d692a-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="d692a-129">See also</span></span>



[<span data-ttu-id="d692a-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d692a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d692a-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d692a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d692a-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d692a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d692a-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d692a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

