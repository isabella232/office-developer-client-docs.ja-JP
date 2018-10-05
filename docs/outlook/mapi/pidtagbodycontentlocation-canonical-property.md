---
title: PidTagBodyContentLocation 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyContentLocation
api_type:
- HeaderDef
ms.assetid: a66d1c64-5c5a-4980-9acd-72448108fd2c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 90a873174b5b990f165d0b2173efa38fc7df2d9d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394918"
---
# <a name="pidtagbodycontentlocation-canonical-property"></a><span data-ttu-id="729f4-103">PidTagBodyContentLocation 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="729f4-103">PidTagBodyContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="729f4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="729f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="729f4-105">MIME コンテンツ場所ヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="729f4-105">Contains the value of a MIME Content-Location header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="729f4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="729f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="729f4-107">PR_BODY_CONTENT_LOCATION、PR_BODY_CONTENT_LOCATION_A、PR_BODY_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="729f4-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="729f4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="729f4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="729f4-109">0x1014</span><span class="sxs-lookup"><span data-stu-id="729f4-109">0x1014</span></span>  <br/> |
|<span data-ttu-id="729f4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="729f4-110">Data type:</span></span>  <br/> |<span data-ttu-id="729f4-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="729f4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="729f4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="729f4-112">Area:</span></span>  <br/> |<span data-ttu-id="729f4-113">MIME</span><span class="sxs-lookup"><span data-stu-id="729f4-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="729f4-114">備考</span><span class="sxs-lookup"><span data-stu-id="729f4-114">Remarks</span></span>

<span data-ttu-id="729f4-115">これらのプロパティの値を設定するのには MIME クライアントに書き込むべき目的の値コンテンツ場所ヘッダー フィールドにメッセージの本文にマップされた MIME エンティティ。</span><span class="sxs-lookup"><span data-stu-id="729f4-115">To set the value of these properties, MIME clients should write the desired value to a Content-Location header field on a MIME entity that maps to a message body.</span></span>
  
<span data-ttu-id="729f4-116">MIME のリーダーは、これらのプロパティの値をこのような MIME エンティティ上のコンテンツ場所ヘッダー フィールドの値をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="729f4-116">MIME readers should copy the value of a Content-Location header field on such a MIME entity to the value of these properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="729f4-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="729f4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="729f4-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="729f4-118">Protocol specifications</span></span>

<span data-ttu-id="729f4-119">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="729f4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="729f4-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="729f4-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="729f4-121">[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="729f4-121">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="729f4-122">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="729f4-122">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="729f4-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="729f4-123">Header files</span></span>

<span data-ttu-id="729f4-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="729f4-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="729f4-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="729f4-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="729f4-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="729f4-126">Mapitags.h</span></span>
  
> <span data-ttu-id="729f4-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="729f4-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="729f4-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="729f4-128">See also</span></span>



[<span data-ttu-id="729f4-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="729f4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="729f4-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="729f4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="729f4-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="729f4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="729f4-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="729f4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

