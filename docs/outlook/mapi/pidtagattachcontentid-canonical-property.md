---
title: PidTagAttachContentId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentId
api_type:
- HeaderDef
ms.assetid: 46f31089-3b66-41a2-8094-e3db52464b9f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 78b157dfb11eb7e97d90142a148e3741e3d818d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572649"
---
# <a name="pidtagattachcontentid-canonical-property"></a><span data-ttu-id="69de3-103">PidTagAttachContentId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="69de3-103">PidTagAttachContentId Canonical Property</span></span>

  
  
<span data-ttu-id="69de3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69de3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69de3-105">多目的インターネット メール拡張 (MIME) メッセージの添付ファイルのコンテンツの識別のヘッダーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="69de3-105">Contains the content identification header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69de3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="69de3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69de3-107">PR_ATTACH_CONTENT_ID、PR_ATTACH_CONTENT_ID_A、PR_ATTACH_CONTENT_ID_W</span><span class="sxs-lookup"><span data-stu-id="69de3-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span></span>  <br/> |
|<span data-ttu-id="69de3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="69de3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69de3-109">0x3712</span><span class="sxs-lookup"><span data-stu-id="69de3-109">0x3712</span></span>  <br/> |
|<span data-ttu-id="69de3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="69de3-110">Data type:</span></span>  <br/> |<span data-ttu-id="69de3-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="69de3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="69de3-112">領域:</span><span class="sxs-lookup"><span data-stu-id="69de3-112">Area:</span></span>  <br/> |<span data-ttu-id="69de3-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="69de3-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69de3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="69de3-114">Remarks</span></span>

<span data-ttu-id="69de3-115">これらのプロパティの使用は、MHTML をサポートするためです。</span><span class="sxs-lookup"><span data-stu-id="69de3-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="69de3-116">適切な MIME ボディ部のコンテンツの識別のヘッダーを表します。</span><span class="sxs-lookup"><span data-stu-id="69de3-116">They represent the content identification header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="69de3-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="69de3-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69de3-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="69de3-118">Protocol specifications</span></span>

<span data-ttu-id="69de3-119">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69de3-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69de3-120">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="69de3-120">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="69de3-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="69de3-121">Header Files</span></span>

<span data-ttu-id="69de3-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69de3-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="69de3-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="69de3-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="69de3-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="69de3-124">Mapitags.h</span></span>
  
> <span data-ttu-id="69de3-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="69de3-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69de3-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="69de3-126">See also</span></span>



[<span data-ttu-id="69de3-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="69de3-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69de3-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="69de3-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69de3-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="69de3-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69de3-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="69de3-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

