---
title: PidTagOrdinalMost 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOrdinalMost
api_type:
- COM
ms.assetid: c18de08b-8c28-4cdf-bd2e-b9c650cd6da6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 31f39cfbd0e993bfc28003fd64e8af97e7e76818
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329188"
---
# <a name="pidtagordinalmost-canonical-property"></a><span data-ttu-id="2ef55-103">PidTagOrdinalMost 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ef55-103">PidTagOrdinalMost Canonical Property</span></span>

  
  
<span data-ttu-id="2ef55-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ef55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ef55-105">負の値がフォルダー内のすべてのタスクの **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) プロパティの値以下の正の数値を含む。</span><span class="sxs-lookup"><span data-stu-id="2ef55-105">Contains a positive number whose negative is less than or equal to the value of the **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) property of all tasks in the folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ef55-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2ef55-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ef55-107">PR_ORDINAL_MOST</span><span class="sxs-lookup"><span data-stu-id="2ef55-107">PR_ORDINAL_MOST</span></span>  <br/> |
|<span data-ttu-id="2ef55-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2ef55-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ef55-109">0x36E2</span><span class="sxs-lookup"><span data-stu-id="2ef55-109">0x36E2</span></span>  <br/> |
|<span data-ttu-id="2ef55-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2ef55-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ef55-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2ef55-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2ef55-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2ef55-112">Area:</span></span>  <br/> |<span data-ttu-id="2ef55-113">タスク</span><span class="sxs-lookup"><span data-stu-id="2ef55-113">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ef55-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2ef55-114">Remarks</span></span>

<span data-ttu-id="2ef55-115">フォルダー内のタスク オブジェクトの **dispidTaskOrdinal** プロパティが条件に違反する方法で変更されるたびに、このプロパティを更新して、この条件を維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ef55-115">This property must be updated to maintain this condition whenever the **dispidTaskOrdinal** property of any task object in the folder changes in a way that would violate the condition.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2ef55-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2ef55-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ef55-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2ef55-117">Protocol specifications</span></span>

<span data-ttu-id="2ef55-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ef55-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ef55-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="2ef55-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2ef55-120">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ef55-120">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ef55-121">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ef55-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
  
### <a name="header-files"></a><span data-ttu-id="2ef55-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2ef55-122">Header files</span></span>

<span data-ttu-id="2ef55-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ef55-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ef55-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ef55-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ef55-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2ef55-125">Mapitags.h</span></span>
  
> <span data-ttu-id="2ef55-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="2ef55-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ef55-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ef55-127">See also</span></span>



[<span data-ttu-id="2ef55-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2ef55-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ef55-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ef55-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ef55-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2ef55-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ef55-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2ef55-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

