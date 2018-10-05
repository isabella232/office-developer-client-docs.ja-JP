---
title: PidTagAttachContentBase 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentBase
api_type:
- HeaderDef
ms.assetid: 35c10264-6998-4c46-8cef-82708c96d9c7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ec1db68d9168e7260a32aaf7708897df6124725a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398977"
---
# <a name="pidtagattachcontentbase-canonical-property"></a><span data-ttu-id="8d5c8-103">PidTagAttachContentBase 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d5c8-103">PidTagAttachContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="8d5c8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d5c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d5c8-105">多目的インターネット メール拡張 (MIME) メッセージの添付ファイルのコンテンツの基本ヘッダーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-105">Contains the content base header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d5c8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8d5c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d5c8-107">PR_ATTACH_CONTENT_BASE、PR_ATTACH_CONTENT_BASE_A、PR_ATTACH_CONTENT_BASE_W</span><span class="sxs-lookup"><span data-stu-id="8d5c8-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span></span>  <br/> |
|<span data-ttu-id="8d5c8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8d5c8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d5c8-109">0x3711</span><span class="sxs-lookup"><span data-stu-id="8d5c8-109">0x3711</span></span>  <br/> |
|<span data-ttu-id="8d5c8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8d5c8-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d5c8-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8d5c8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8d5c8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8d5c8-112">Area:</span></span>  <br/> |<span data-ttu-id="8d5c8-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="8d5c8-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d5c8-114">備考</span><span class="sxs-lookup"><span data-stu-id="8d5c8-114">Remarks</span></span>

<span data-ttu-id="8d5c8-115">これらのプロパティの使用は、MHTML をサポートするためです。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="8d5c8-116">適切な MIME ボディ部のコンテンツ ベースのヘッダーを表します。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-116">They represent the content base header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8d5c8-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8d5c8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d5c8-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8d5c8-118">Protocol specifications</span></span>

<span data-ttu-id="8d5c8-119">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d5c8-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d5c8-120">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d5c8-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8d5c8-121">Header files</span></span>

<span data-ttu-id="8d5c8-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d5c8-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d5c8-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d5c8-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d5c8-124">Mapitags.h</span></span>
  
> <span data-ttu-id="8d5c8-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d5c8-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d5c8-126">See also</span></span>



[<span data-ttu-id="8d5c8-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d5c8-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d5c8-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d5c8-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d5c8-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8d5c8-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d5c8-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8d5c8-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

