---
title: PidTagOriginalDisplayTo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayTo
api_type:
- COM
ms.assetid: 8c1cf14c-0339-4ced-8f68-4bfaa1e4d3e9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5a2f60051e5cb0717926a5c3e2f878a49919b04c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342702"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a><span data-ttu-id="aba74-103">PidTagOriginalDisplayTo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aba74-103">PidTagOriginalDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="aba74-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aba74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aba74-105">元のメッセージのプライマリ (宛先) 受信者の表示名を格納します。</span><span class="sxs-lookup"><span data-stu-id="aba74-105">Contains the display names of the primary (To) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aba74-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="aba74-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aba74-107">PR_ORIGINAL_DISPLAY_TO、PR_ORIGINAL_DISPLAY_TO_A、PR_ORIGINAL_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="aba74-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="aba74-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="aba74-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aba74-109">0x0074</span><span class="sxs-lookup"><span data-stu-id="aba74-109">0x0074</span></span>  <br/> |
|<span data-ttu-id="aba74-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="aba74-110">Data type:</span></span>  <br/> |<span data-ttu-id="aba74-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aba74-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="aba74-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="aba74-112">Area:</span></span>  <br/> |<span data-ttu-id="aba74-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="aba74-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aba74-114">注釈</span><span class="sxs-lookup"><span data-stu-id="aba74-114">Remarks</span></span>

<span data-ttu-id="aba74-115">これらのプロパティには、セミコロンで区切られた ASCII リストが含まれる。</span><span class="sxs-lookup"><span data-stu-id="aba74-115">These properties contain an ASCII list separated by semicolons.</span></span> <span data-ttu-id="aba74-116">これは MAPI によって提供され、配信レポートまたは配信不能レポートまたは読み取りレポートまたは未読レポートが生成されると **、PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) から直接コピーされます。</span><span class="sxs-lookup"><span data-stu-id="aba74-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="aba74-117">このプロパティは、メッセージ クラスで定義されている他のメッセージに存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="aba74-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aba74-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="aba74-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aba74-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="aba74-119">Protocol specifications</span></span>

<span data-ttu-id="aba74-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aba74-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aba74-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="aba74-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aba74-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aba74-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aba74-123">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="aba74-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aba74-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="aba74-124">Header files</span></span>

<span data-ttu-id="aba74-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aba74-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="aba74-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="aba74-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="aba74-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aba74-127">Mapitags.h</span></span>
  
> <span data-ttu-id="aba74-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="aba74-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aba74-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="aba74-129">See also</span></span>



[<span data-ttu-id="aba74-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="aba74-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aba74-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aba74-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aba74-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="aba74-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aba74-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="aba74-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

