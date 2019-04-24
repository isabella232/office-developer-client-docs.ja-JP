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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5a2f60051e5cb0717926a5c3e2f878a49919b04c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342702"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a><span data-ttu-id="f01ea-103">PidTagOriginalDisplayTo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f01ea-103">PidTagOriginalDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="f01ea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f01ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f01ea-105">元のメッセージのプライマリ (宛先) 受信者の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f01ea-105">Contains the display names of the primary (To) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f01ea-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f01ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f01ea-107">PR_ORIGINAL_DISPLAY_TO、PR_ORIGINAL_DISPLAY_TO_A、PR_ORIGINAL_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="f01ea-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="f01ea-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f01ea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f01ea-109">0x0074</span><span class="sxs-lookup"><span data-stu-id="f01ea-109">0x0074</span></span>  <br/> |
|<span data-ttu-id="f01ea-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f01ea-110">Data type:</span></span>  <br/> |<span data-ttu-id="f01ea-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f01ea-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f01ea-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f01ea-112">Area:</span></span>  <br/> |<span data-ttu-id="f01ea-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="f01ea-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f01ea-114">解説</span><span class="sxs-lookup"><span data-stu-id="f01ea-114">Remarks</span></span>

<span data-ttu-id="f01ea-115">これらのプロパティには、セミコロンで区切られた ASCII リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f01ea-115">These properties contain an ASCII list separated by semicolons.</span></span> <span data-ttu-id="f01ea-116">これは MAPI によって提供され、配信レポートまたは配信不能レポートまたは読み取りまたは非開封レポートが生成されたときに、 **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) から直接コピーされます。</span><span class="sxs-lookup"><span data-stu-id="f01ea-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="f01ea-117">このプロパティは、メッセージクラスによって定義されている他のメッセージに表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="f01ea-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f01ea-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f01ea-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f01ea-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f01ea-119">Protocol specifications</span></span>

<span data-ttu-id="f01ea-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f01ea-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f01ea-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f01ea-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f01ea-122">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f01ea-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f01ea-123">電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f01ea-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f01ea-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="f01ea-124">Header files</span></span>

<span data-ttu-id="f01ea-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f01ea-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f01ea-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f01ea-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f01ea-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="f01ea-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f01ea-128">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f01ea-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f01ea-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="f01ea-129">See also</span></span>



[<span data-ttu-id="f01ea-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f01ea-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f01ea-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f01ea-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f01ea-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f01ea-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f01ea-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f01ea-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

