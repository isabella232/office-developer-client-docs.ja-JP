---
title: PidTagInternetReferences 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b0e01d3f56ef01984f281e7fae5990ccb0eade88
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593334"
---
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="006e2-103">PidTagInternetReferences 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="006e2-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="006e2-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="006e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="006e2-105">多目的インターネット メール拡張 (MIME) メッセージの参照のヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="006e2-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="006e2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="006e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="006e2-107">PR_INTERNET_REFERENCES、PR_INTERNET_REFERENCES_A、PR_INTERNET_REFERENCES_W</span><span class="sxs-lookup"><span data-stu-id="006e2-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="006e2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="006e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="006e2-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="006e2-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="006e2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="006e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="006e2-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="006e2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="006e2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="006e2-112">Area:</span></span>  <br/> |<span data-ttu-id="006e2-113">MIME</span><span class="sxs-lookup"><span data-stu-id="006e2-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="006e2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="006e2-114">Remarks</span></span>

<span data-ttu-id="006e2-115">参照ヘッダー フィールドを生成するには、クライアントは、目的の値にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="006e2-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="006e2-116">MIME ライターは、参照のヘッダー フィールドにこれらのプロパティの値をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="006e2-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="006e2-117">これらのプロパティの値を設定するのには MIME クライアントは、参照のヘッダー フィールドに目的の値を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="006e2-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="006e2-118">MIME のリーダーは、これらのプロパティへの参照のヘッダー フィールドの値をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="006e2-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="006e2-119">長さは 64 KB を超えている場合、MIME のリーダーはこれらのプロパティの値を切り捨てることがあります。</span><span class="sxs-lookup"><span data-stu-id="006e2-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="006e2-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="006e2-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="006e2-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="006e2-121">Protocol specifications</span></span>

<span data-ttu-id="006e2-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="006e2-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="006e2-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="006e2-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="006e2-124">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="006e2-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="006e2-125">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="006e2-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="006e2-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="006e2-126">Header files</span></span>

<span data-ttu-id="006e2-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="006e2-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="006e2-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="006e2-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="006e2-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="006e2-129">Mapitags.h</span></span>
  
> <span data-ttu-id="006e2-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="006e2-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="006e2-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="006e2-131">See also</span></span>



[<span data-ttu-id="006e2-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="006e2-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="006e2-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="006e2-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="006e2-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="006e2-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="006e2-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="006e2-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

