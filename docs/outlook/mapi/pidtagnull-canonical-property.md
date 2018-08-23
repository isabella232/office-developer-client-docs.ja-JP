---
title: PidTagNull 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: efb0812a88ad435c2456a729a6e950b371cc0250
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595350"
---
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="6802d-103">PidTagNull 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6802d-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="6802d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6802d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6802d-105">配列の領域を予約または、null 値またはプロパティの設定を表します。</span><span class="sxs-lookup"><span data-stu-id="6802d-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6802d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6802d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6802d-107">PR_NULL</span><span class="sxs-lookup"><span data-stu-id="6802d-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="6802d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6802d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6802d-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="6802d-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="6802d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6802d-110">Data type:</span></span>  <br/> |<span data-ttu-id="6802d-111">PT_NULL</span><span class="sxs-lookup"><span data-stu-id="6802d-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="6802d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6802d-112">Area:</span></span>  <br/> |<span data-ttu-id="6802d-113">Common</span><span class="sxs-lookup"><span data-stu-id="6802d-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6802d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6802d-114">Remarks</span></span>

<span data-ttu-id="6802d-115">[SPropValue](spropvalue.md)構造体の配列の領域を予約するのにはこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="6802d-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="6802d-116">**SPropValue**構造体の返される配列内の領域を予約する方法を指示する[SPropTagArray](sproptagarray.md)構造体の配列で使用されます。</span><span class="sxs-lookup"><span data-stu-id="6802d-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="6802d-117">安価な方法で設定されるプロパティを計算できます。</span><span class="sxs-lookup"><span data-stu-id="6802d-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="6802d-118">詳細については、 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6802d-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6802d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6802d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6802d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6802d-120">Protocol specifications</span></span>

<span data-ttu-id="6802d-121">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6802d-121">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6802d-122">連絡先と個人用配布リストで許可されている操作のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="6802d-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6802d-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6802d-123">Header files</span></span>

<span data-ttu-id="6802d-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6802d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6802d-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6802d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6802d-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6802d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6802d-127">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6802d-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6802d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="6802d-128">See also</span></span>



[<span data-ttu-id="6802d-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6802d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6802d-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6802d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6802d-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6802d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6802d-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6802d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

