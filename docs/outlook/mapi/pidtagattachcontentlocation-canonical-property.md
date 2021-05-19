---
title: PidTagAttachContentLocation 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentLocation
api_type:
- HeaderDef
ms.assetid: af2f776c-1b77-4942-827a-4363eda3924f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f279d8ea305c0b1e609881b15e39653c41d5828e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345480"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="80e46-103">PidTagAttachContentLocation 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="80e46-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="80e46-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80e46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80e46-105">多目的インターネット メール拡張機能 (MIME) メッセージ添付ファイルのコンテンツの場所ヘッダーを格納します。</span><span class="sxs-lookup"><span data-stu-id="80e46-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="80e46-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="80e46-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80e46-107">PR_ATTACH_CONTENT_LOCATION、PR_ATTACH_CONTENT_LOCATION_A、PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="80e46-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="80e46-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="80e46-108">Identifier:</span></span>  <br/> |<span data-ttu-id="80e46-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="80e46-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="80e46-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="80e46-110">Data type:</span></span>  <br/> |<span data-ttu-id="80e46-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="80e46-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="80e46-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="80e46-112">Area:</span></span>  <br/> |<span data-ttu-id="80e46-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="80e46-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80e46-114">注釈</span><span class="sxs-lookup"><span data-stu-id="80e46-114">Remarks</span></span>

<span data-ttu-id="80e46-115">これらのプロパティは、MHTML のサポートに使用されます。</span><span class="sxs-lookup"><span data-stu-id="80e46-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="80e46-116">これらは、適切な MIME 本文パーツのコンテンツの場所ヘッダーを表します。</span><span class="sxs-lookup"><span data-stu-id="80e46-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="80e46-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="80e46-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80e46-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="80e46-118">Protocol specifications</span></span>

<span data-ttu-id="80e46-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80e46-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80e46-120">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="80e46-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80e46-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="80e46-121">Header files</span></span>

<span data-ttu-id="80e46-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80e46-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="80e46-123">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="80e46-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="80e46-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="80e46-124">Mapitags.h</span></span>
  
> <span data-ttu-id="80e46-125">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="80e46-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80e46-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="80e46-126">See also</span></span>



[<span data-ttu-id="80e46-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="80e46-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80e46-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="80e46-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80e46-129">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="80e46-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80e46-130">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="80e46-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

