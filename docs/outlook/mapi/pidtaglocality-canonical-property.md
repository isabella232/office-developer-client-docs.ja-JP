---
title: PidTagLocality 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLocality
api_type:
- HeaderDef
ms.assetid: a918b596-a335-47a0-9d1c-109a0b0812a2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 27c9ab646d6a03d63aa2b5a6820f9c3023186d8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574602"
---
# <a name="pidtaglocality-canonical-property"></a><span data-ttu-id="cca2d-103">PidTagLocality 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cca2d-103">PidTagLocality Canonical Property</span></span>

  
  
<span data-ttu-id="cca2d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cca2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cca2d-105">市区町村など、受信者の局所性の名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cca2d-105">Contains the name of the recipient's locality, such as the town or city.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cca2d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="cca2d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cca2d-107">PR_LOCALITY、PR_LOCALITY_A、PR_LOCALITY_W、PR_BUSINESS_ADDRESS_LOCALITY、PR_BUSINESS_ADDRESS_LOCALITY_A、PR_BUSINESS_ADDRESS_LOCALITY_W</span><span class="sxs-lookup"><span data-stu-id="cca2d-107">PR_LOCALITY, PR_LOCALITY_A, PR_LOCALITY_W, PR_BUSINESS_ADDRESS_LOCALITY, PR_BUSINESS_ADDRESS_LOCALITY_A, PR_BUSINESS_ADDRESS_LOCALITY_W</span></span>  <br/> |
|<span data-ttu-id="cca2d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cca2d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cca2d-109">0x3A27</span><span class="sxs-lookup"><span data-stu-id="cca2d-109">0x3A27</span></span>  <br/> |
|<span data-ttu-id="cca2d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="cca2d-110">Data type:</span></span>  <br/> |<span data-ttu-id="cca2d-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="cca2d-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="cca2d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="cca2d-112">Area:</span></span>  <br/> |<span data-ttu-id="cca2d-113">Address</span><span class="sxs-lookup"><span data-stu-id="cca2d-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cca2d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="cca2d-114">Remarks</span></span>

<span data-ttu-id="cca2d-115">これらのプロパティでは、識別を提供し、受信者の情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="cca2d-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="cca2d-116">Theys は、受信者とその構造によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="cca2d-116">Theys are defined by the recipient and their organization.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cca2d-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cca2d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cca2d-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cca2d-118">Protocol specifications</span></span>

<span data-ttu-id="cca2d-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cca2d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cca2d-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cca2d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cca2d-121">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cca2d-121">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cca2d-122">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="cca2d-122">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="cca2d-123">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cca2d-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cca2d-124">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="cca2d-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cca2d-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="cca2d-125">Header files</span></span>

<span data-ttu-id="cca2d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cca2d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="cca2d-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cca2d-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="cca2d-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cca2d-128">Mapitags.h</span></span>
  
> <span data-ttu-id="cca2d-129">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cca2d-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cca2d-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="cca2d-130">See also</span></span>



[<span data-ttu-id="cca2d-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cca2d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cca2d-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cca2d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cca2d-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cca2d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cca2d-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cca2d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

