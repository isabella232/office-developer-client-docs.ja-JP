---
title: PidTagOriginalDisplayBcc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayBcc
api_type:
- COM
ms.assetid: 7bf66f0c-3095-4b4a-a32e-db278e1adc5a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3fbd7205901616695bcdcd012601afd252ac05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355644"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a><span data-ttu-id="fa644-103">PidTagOriginalDisplayBcc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fa644-103">PidTagOriginalDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="fa644-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa644-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa644-105">元のメッセージの bcc (ブラインドカーボンコピー) 受信者の表示名が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fa644-105">Contains the display names of any blind carbon copy (BCC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa644-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fa644-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fa644-107">PR_ORIGINAL_DISPLAY_BCC、PR_ORIGINAL_DISPLAY_BCC_A、PR_ORIGINAL_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="fa644-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="fa644-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fa644-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fa644-109">0x0072</span><span class="sxs-lookup"><span data-stu-id="fa644-109">0x0072</span></span>  <br/> |
|<span data-ttu-id="fa644-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fa644-110">Data type:</span></span>  <br/> |<span data-ttu-id="fa644-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fa644-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fa644-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="fa644-112">Area:</span></span>  <br/> |<span data-ttu-id="fa644-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="fa644-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa644-114">解説</span><span class="sxs-lookup"><span data-stu-id="fa644-114">Remarks</span></span>

<span data-ttu-id="fa644-115">これらのプロパティには、セミコロンで区切られたリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fa644-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="fa644-116">これらは MAPI によって提供され、配信レポートまたは配信不能レポートまたは読み取りまたは非開封レポートが生成されたときに、 **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) から直接コピーされます。</span><span class="sxs-lookup"><span data-stu-id="fa644-116">They is furnished by MAPI and are copied directly from **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="fa644-117">これらのプロパティは、メッセージクラスによって定義されている他のメッセージに表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="fa644-117">These properties may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fa644-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fa644-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fa644-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fa644-119">Protocol specifications</span></span>

<span data-ttu-id="fa644-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa644-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa644-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fa644-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fa644-122">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa644-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa644-123">電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="fa644-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fa644-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="fa644-124">Header files</span></span>

<span data-ttu-id="fa644-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa644-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fa644-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fa644-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="fa644-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="fa644-127">Mapitags.h</span></span>
  
> <span data-ttu-id="fa644-128">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fa644-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa644-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa644-129">See also</span></span>



[<span data-ttu-id="fa644-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fa644-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fa644-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fa644-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fa644-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fa644-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fa644-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fa644-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

