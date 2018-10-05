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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396716"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a><span data-ttu-id="f575c-103">PidTagOriginalDisplayBcc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f575c-103">PidTagOriginalDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="f575c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f575c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f575c-105">元のメッセージのブラインド カーボン コピー (BCC) 受信者の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f575c-105">Contains the display names of any blind carbon copy (BCC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f575c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f575c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f575c-107">PR_ORIGINAL_DISPLAY_BCC、PR_ORIGINAL_DISPLAY_BCC_A、PR_ORIGINAL_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="f575c-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="f575c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f575c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f575c-109">0x0072</span><span class="sxs-lookup"><span data-stu-id="f575c-109">0x0072</span></span>  <br/> |
|<span data-ttu-id="f575c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f575c-110">Data type:</span></span>  <br/> |<span data-ttu-id="f575c-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f575c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f575c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f575c-112">Area:</span></span>  <br/> |<span data-ttu-id="f575c-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="f575c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f575c-114">備考</span><span class="sxs-lookup"><span data-stu-id="f575c-114">Remarks</span></span>

<span data-ttu-id="f575c-115">これらのプロパティには、セミコロンで区切られたリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f575c-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="f575c-116">MAPI によって提供されて、配信または配信不能レポート、読み取りまたは nonread のレポートが生成されるときに、 **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) から直接コピーされます。</span><span class="sxs-lookup"><span data-stu-id="f575c-116">They is furnished by MAPI and are copied directly from **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="f575c-117">これらのプロパティは、他のメッセージをそのメッセージ クラスで定義されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f575c-117">These properties may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f575c-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f575c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f575c-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f575c-119">Protocol specifications</span></span>

<span data-ttu-id="f575c-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f575c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f575c-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f575c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f575c-122">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f575c-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f575c-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f575c-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f575c-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f575c-124">Header files</span></span>

<span data-ttu-id="f575c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f575c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f575c-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f575c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f575c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f575c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f575c-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f575c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f575c-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="f575c-129">See also</span></span>



[<span data-ttu-id="f575c-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f575c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f575c-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f575c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f575c-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f575c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f575c-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f575c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

