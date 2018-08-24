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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1d654c2a14728979146ef09618bfc4e9e618f9d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594769"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="8b928-103">PidTagAttachContentLocation 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8b928-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="8b928-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b928-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b928-105">多目的インターネット メール拡張 (MIME) メッセージの添付ファイルのコンテンツの場所のヘッダーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8b928-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b928-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8b928-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b928-107">PR_ATTACH_CONTENT_LOCATION、PR_ATTACH_CONTENT_LOCATION_A、PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="8b928-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="8b928-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8b928-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b928-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="8b928-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="8b928-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8b928-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b928-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8b928-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8b928-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8b928-112">Area:</span></span>  <br/> |<span data-ttu-id="8b928-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="8b928-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b928-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8b928-114">Remarks</span></span>

<span data-ttu-id="8b928-115">これらのプロパティの使用は、MHTML をサポートするためです。</span><span class="sxs-lookup"><span data-stu-id="8b928-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="8b928-116">適切な MIME ボディ部のコンテンツ場所ヘッダーを表します。</span><span class="sxs-lookup"><span data-stu-id="8b928-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8b928-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8b928-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b928-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8b928-118">Protocol specifications</span></span>

<span data-ttu-id="8b928-119">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b928-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b928-120">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="8b928-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b928-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8b928-121">Header files</span></span>

<span data-ttu-id="8b928-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b928-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b928-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8b928-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b928-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8b928-124">Mapitags.h</span></span>
  
> <span data-ttu-id="8b928-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8b928-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b928-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="8b928-126">See also</span></span>



[<span data-ttu-id="8b928-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8b928-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b928-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8b928-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b928-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8b928-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b928-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8b928-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

