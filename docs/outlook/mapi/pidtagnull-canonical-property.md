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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329268"
---
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="4b401-103">PidTagNull 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4b401-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="4b401-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b401-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b401-105">プロパティの null 値または設定を表す、または配列スペースを予約します。</span><span class="sxs-lookup"><span data-stu-id="4b401-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b401-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4b401-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b401-107">PR_NULL</span><span class="sxs-lookup"><span data-stu-id="4b401-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="4b401-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4b401-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4b401-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="4b401-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="4b401-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4b401-110">Data type:</span></span>  <br/> |<span data-ttu-id="4b401-111">PT_NULL</span><span class="sxs-lookup"><span data-stu-id="4b401-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="4b401-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4b401-112">Area:</span></span>  <br/> |<span data-ttu-id="4b401-113">共通</span><span class="sxs-lookup"><span data-stu-id="4b401-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b401-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4b401-114">Remarks</span></span>

<span data-ttu-id="4b401-115">このプロパティは [、SPropValue](spropvalue.md) 構造体の配列内の領域を予約するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4b401-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="4b401-116">[SPropTagArray](sproptagarray.md)構造体の配列で使用して、返される **SPropValue** 構造体の配列にスペースを予約するメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="4b401-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="4b401-117">これにより、計算されたプロパティを安価な方法で入力できます。</span><span class="sxs-lookup"><span data-stu-id="4b401-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="4b401-118">詳細については、「MAPI プロパティの [種類の概要」を参照してください](mapi-property-type-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="4b401-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4b401-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4b401-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4b401-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4b401-120">Protocol specifications</span></span>

<span data-ttu-id="4b401-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b401-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b401-122">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4b401-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4b401-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4b401-123">Header files</span></span>

<span data-ttu-id="4b401-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b401-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b401-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4b401-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4b401-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4b401-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4b401-127">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="4b401-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b401-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b401-128">See also</span></span>



[<span data-ttu-id="4b401-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4b401-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b401-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4b401-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b401-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="4b401-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b401-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="4b401-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

