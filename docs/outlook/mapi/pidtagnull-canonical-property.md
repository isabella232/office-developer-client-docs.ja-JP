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
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329268"
---
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="78875-103">PidTagNull 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="78875-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="78875-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78875-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78875-105">null 値またはプロパティの設定を表します。または、配列スペースを予約します。</span><span class="sxs-lookup"><span data-stu-id="78875-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78875-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="78875-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="78875-107">PR_NULL</span><span class="sxs-lookup"><span data-stu-id="78875-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="78875-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="78875-108">Identifier:</span></span>  <br/> |<span data-ttu-id="78875-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="78875-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="78875-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="78875-110">Data type:</span></span>  <br/> |<span data-ttu-id="78875-111">PT_NULL</span><span class="sxs-lookup"><span data-stu-id="78875-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="78875-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="78875-112">Area:</span></span>  <br/> |<span data-ttu-id="78875-113">共通</span><span class="sxs-lookup"><span data-stu-id="78875-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78875-114">解説</span><span class="sxs-lookup"><span data-stu-id="78875-114">Remarks</span></span>

<span data-ttu-id="78875-115">このプロパティは、 [spropvalue](spropvalue.md)構造の配列にスペースを予約するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="78875-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="78875-116">[SPropTagArray](sproptagarray.md)構造体の配列で使用され、 **spropvalue**構造の返された配列にスペースを予約することをメソッドに通知します。</span><span class="sxs-lookup"><span data-stu-id="78875-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="78875-117">これにより、計算されたプロパティを安価な方法で入力することができます。</span><span class="sxs-lookup"><span data-stu-id="78875-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="78875-118">詳細については、「 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78875-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="78875-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="78875-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="78875-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="78875-120">Protocol specifications</span></span>

<span data-ttu-id="78875-121">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78875-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78875-122">連絡先および個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="78875-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="78875-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="78875-123">Header files</span></span>

<span data-ttu-id="78875-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78875-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="78875-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="78875-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="78875-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="78875-126">Mapitags.h</span></span>
  
> <span data-ttu-id="78875-127">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="78875-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78875-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="78875-128">See also</span></span>



[<span data-ttu-id="78875-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="78875-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78875-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="78875-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78875-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="78875-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78875-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="78875-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

