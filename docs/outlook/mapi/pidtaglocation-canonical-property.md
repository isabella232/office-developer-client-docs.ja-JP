---
title: PidTagLocation 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLocation
api_type:
- HeaderDef
ms.assetid: 99dffcd9-83dc-462e-b0ce-e2101e546cc6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 03082536902ead880ba88343cd1991e518ed5665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802955"
---
# <a name="pidtaglocation-canonical-property"></a><span data-ttu-id="6889a-103">PidTagLocation 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6889a-103">PidTagLocation Canonical Property</span></span>

  
  
<span data-ttu-id="6889a-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6889a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6889a-105">受信者の組織に役に立つ形式で受信者の場所が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6889a-105">Contains the location of the recipient in a format that is useful to the recipient's organization.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6889a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6889a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6889a-107">PR_LOCATION、PR_LOCATION_A、PR_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="6889a-107">PR_LOCATION, PR_LOCATION_A, PR_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="6889a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6889a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6889a-109">0x3A0D</span><span class="sxs-lookup"><span data-stu-id="6889a-109">0x3A0D</span></span>  <br/> |
|<span data-ttu-id="6889a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6889a-110">Data type:</span></span>  <br/> |<span data-ttu-id="6889a-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="6889a-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="6889a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6889a-112">Area:</span></span>  <br/> |<span data-ttu-id="6889a-113">Address</span><span class="sxs-lookup"><span data-stu-id="6889a-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6889a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6889a-114">Remarks</span></span>

<span data-ttu-id="6889a-115">これらのプロパティでは、識別を提供し、受信者の情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="6889a-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="6889a-116">受信者とその構造によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="6889a-116">They are defined by the recipient and their organization.</span></span> 
  
<span data-ttu-id="6889a-117">内容は、受信者の組織のニーズによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="6889a-117">The contents are defined by the needs of the recipient's organization.</span></span> <span data-ttu-id="6889a-118">などの一部の組織では、建物の番号とオフィス番号を指定することでメッセージング ユーザーを識別する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6889a-118">For example, some organizations might identify messaging users by specifying the building number and office number.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6889a-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6889a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6889a-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6889a-120">Protocol specifications</span></span>

<span data-ttu-id="6889a-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6889a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6889a-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6889a-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6889a-123">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6889a-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6889a-124">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6889a-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="6889a-125">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6889a-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6889a-126">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6889a-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6889a-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6889a-127">Header files</span></span>

<span data-ttu-id="6889a-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6889a-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="6889a-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6889a-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="6889a-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6889a-130">Mapitags.h</span></span>
  
> <span data-ttu-id="6889a-131">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6889a-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6889a-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="6889a-132">See also</span></span>



[<span data-ttu-id="6889a-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6889a-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6889a-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6889a-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6889a-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6889a-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6889a-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6889a-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

