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
ms.openlocfilehash: 5fc7360e3070ed4d20be7ac0155ebdcb04cf2048
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319209"
---
# <a name="pidtagattachcontentid-canonical-property"></a><span data-ttu-id="00f49-103">PidTagAttachContentId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="00f49-103">PidTagAttachContentId Canonical Property</span></span>

  
  
<span data-ttu-id="00f49-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00f49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00f49-105">マルチパーパスインターネットメール内線 (MIME) メッセージの添付ファイルのコンテンツ id ヘッダーを含みます。</span><span class="sxs-lookup"><span data-stu-id="00f49-105">Contains the content identification header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00f49-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="00f49-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00f49-107">PR_ATTACH_CONTENT_ID、PR_ATTACH_CONTENT_ID_A、PR_ATTACH_CONTENT_ID_W</span><span class="sxs-lookup"><span data-stu-id="00f49-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span></span>  <br/> |
|<span data-ttu-id="00f49-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="00f49-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00f49-109">0x3712</span><span class="sxs-lookup"><span data-stu-id="00f49-109">0x3712</span></span>  <br/> |
|<span data-ttu-id="00f49-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="00f49-110">Data type:</span></span>  <br/> |<span data-ttu-id="00f49-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="00f49-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="00f49-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="00f49-112">Area:</span></span>  <br/> |<span data-ttu-id="00f49-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="00f49-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00f49-114">解説</span><span class="sxs-lookup"><span data-stu-id="00f49-114">Remarks</span></span>

<span data-ttu-id="00f49-115">これらのプロパティは、MHTML のサポートに使用されます。</span><span class="sxs-lookup"><span data-stu-id="00f49-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="00f49-116">これらは、適切な MIME 本文パーツのコンテンツ id ヘッダーを表します。</span><span class="sxs-lookup"><span data-stu-id="00f49-116">They represent the content identification header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="00f49-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="00f49-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00f49-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="00f49-118">Protocol specifications</span></span>

<span data-ttu-id="00f49-119">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00f49-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00f49-120">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="00f49-120">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="00f49-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="00f49-121">Header Files</span></span>

<span data-ttu-id="00f49-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00f49-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="00f49-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="00f49-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="00f49-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="00f49-124">Mapitags.h</span></span>
  
> <span data-ttu-id="00f49-125">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="00f49-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00f49-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="00f49-126">See also</span></span>



[<span data-ttu-id="00f49-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="00f49-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00f49-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="00f49-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00f49-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="00f49-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00f49-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="00f49-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

