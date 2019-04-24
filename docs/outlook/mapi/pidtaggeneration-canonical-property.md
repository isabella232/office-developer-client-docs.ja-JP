---
title: PidTagGeneration 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGeneration
api_type:
- HeaderDef
ms.assetid: 81c2e479-84a1-42ba-a9ce-25e3fc8d80cb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f8a2c92e47c2f309cd52f80c0cb5cf5d1f3518e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316136"
---
# <a name="pidtaggeneration-canonical-property"></a><span data-ttu-id="64a36-103">PidTagGeneration 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="64a36-103">PidTagGeneration Canonical Property</span></span>

  
  
<span data-ttu-id="64a36-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64a36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64a36-105">受信者の完全な名前の後の省略形が含まれています。</span><span class="sxs-lookup"><span data-stu-id="64a36-105">Contains a generational abbreviation that follows the full name of the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64a36-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="64a36-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64a36-107">PR_GENERATION、PR_GENERATION_A、PR_GENERATION_W</span><span class="sxs-lookup"><span data-stu-id="64a36-107">PR_GENERATION, PR_GENERATION_A, PR_GENERATION_W</span></span>  <br/> |
|<span data-ttu-id="64a36-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="64a36-108">Identifier:</span></span>  <br/> |<span data-ttu-id="64a36-109">0x3a05</span><span class="sxs-lookup"><span data-stu-id="64a36-109">0x3A05</span></span>  <br/> |
|<span data-ttu-id="64a36-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="64a36-110">Data type:</span></span>  <br/> |<span data-ttu-id="64a36-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="64a36-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="64a36-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="64a36-112">Area:</span></span>  <br/> |<span data-ttu-id="64a36-113">MAPI メールユーザー</span><span class="sxs-lookup"><span data-stu-id="64a36-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64a36-114">解説</span><span class="sxs-lookup"><span data-stu-id="64a36-114">Remarks</span></span>

<span data-ttu-id="64a36-115">これらのプロパティは、受信者に関する id とアクセス情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="64a36-115">These properties provide identification and access information about a recipient.</span></span> <span data-ttu-id="64a36-116">受信者と組織で定義されています。</span><span class="sxs-lookup"><span data-stu-id="64a36-116">They are defined by the recipient and their organization.</span></span> 
  
<span data-ttu-id="64a36-117">一般的な値には、ジュニア、Sr、および III があります。</span><span class="sxs-lookup"><span data-stu-id="64a36-117">Common values include Jr., Sr., and III.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="64a36-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="64a36-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64a36-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="64a36-119">Protocol specifications</span></span>

<span data-ttu-id="64a36-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64a36-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64a36-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="64a36-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64a36-122">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64a36-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64a36-123">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="64a36-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="64a36-124">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64a36-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64a36-125">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="64a36-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64a36-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="64a36-126">Header files</span></span>

<span data-ttu-id="64a36-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64a36-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="64a36-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="64a36-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="64a36-129">Mapitags</span><span class="sxs-lookup"><span data-stu-id="64a36-129">Mapitags.h</span></span>
  
> <span data-ttu-id="64a36-130">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="64a36-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64a36-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="64a36-131">See also</span></span>



[<span data-ttu-id="64a36-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="64a36-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64a36-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="64a36-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64a36-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="64a36-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64a36-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="64a36-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

