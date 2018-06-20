---
title: PidTagBodyContentLocation の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a05743f2fa10326a358dd92a72cf530740274f2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802544"
---
# <a name="pidtagbodycontentlocation-canonical-property"></a><span data-ttu-id="b59e0-103">PidTagBodyContentLocation の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b59e0-103">PidTagBodyContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="b59e0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b59e0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b59e0-105">MIME コンテンツ場所ヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b59e0-105">Contains the value of a MIME Content-Location header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b59e0-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b59e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b59e0-107">PR_BODY_CONTENT_LOCATION、PR_BODY_CONTENT_LOCATION_A、PR_BODY_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="b59e0-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="b59e0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b59e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b59e0-109">0x1014</span><span class="sxs-lookup"><span data-stu-id="b59e0-109">0x1014</span></span>  <br/> |
|<span data-ttu-id="b59e0-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="b59e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="b59e0-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b59e0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b59e0-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b59e0-112">Area:</span></span>  <br/> |<span data-ttu-id="b59e0-113">MIME</span><span class="sxs-lookup"><span data-stu-id="b59e0-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b59e0-114">備考</span><span class="sxs-lookup"><span data-stu-id="b59e0-114">Remarks</span></span>

<span data-ttu-id="b59e0-115">これらのプロパティの値を設定するのには MIME クライアントに書き込むべき目的の値コンテンツ場所ヘッダー フィールドにメッセージの本文にマップされた MIME エンティティ。</span><span class="sxs-lookup"><span data-stu-id="b59e0-115">To set the value of these properties, MIME clients should write the desired value to a Content-Location header field on a MIME entity that maps to a message body.</span></span>
  
<span data-ttu-id="b59e0-116">MIME のリーダーは、これらのプロパティの値をこのような MIME エンティティ上のコンテンツ場所ヘッダー フィールドの値をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b59e0-116">MIME readers should copy the value of a Content-Location header field on such a MIME entity to the value of these properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b59e0-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b59e0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b59e0-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b59e0-118">Protocol specifications</span></span>

<span data-ttu-id="b59e0-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b59e0-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b59e0-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b59e0-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b59e0-121">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b59e0-121">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b59e0-122">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="b59e0-122">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b59e0-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b59e0-123">Header files</span></span>

<span data-ttu-id="b59e0-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b59e0-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="b59e0-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b59e0-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="b59e0-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b59e0-126">Mapitags.h</span></span>
  
> <span data-ttu-id="b59e0-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b59e0-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b59e0-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b59e0-128">See also</span></span>



[<span data-ttu-id="b59e0-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b59e0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b59e0-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b59e0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b59e0-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="b59e0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b59e0-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="b59e0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

