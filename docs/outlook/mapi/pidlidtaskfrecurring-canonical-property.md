---
title: PidLidTaskFRecurring 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFRecurring
api_type:
- COM
ms.assetid: 47c9ccbb-161c-4829-8ffb-201f3b54cd45
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: aec9dd328e802e185c870d3ecd94cbd1d10ac67d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303053"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a><span data-ttu-id="353d2-103">PidLidTaskFRecurring 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="353d2-103">PidLidTaskFRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="353d2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="353d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="353d2-105">タスクに定期的なパターンが含まれるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="353d2-105">Indicates whether the task includes a recurrence pattern.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="353d2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="353d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="353d2-107">dispidTaskFRecur</span><span class="sxs-lookup"><span data-stu-id="353d2-107">dispidTaskFRecur</span></span>  <br/> |
|<span data-ttu-id="353d2-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="353d2-108">Property set:</span></span>  <br/> |<span data-ttu-id="353d2-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="353d2-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="353d2-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="353d2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="353d2-111">0x00008126</span><span class="sxs-lookup"><span data-stu-id="353d2-111">0x00008126</span></span>  <br/> |
|<span data-ttu-id="353d2-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="353d2-112">Data type:</span></span>  <br/> |<span data-ttu-id="353d2-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="353d2-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="353d2-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="353d2-114">Area:</span></span>  <br/> |<span data-ttu-id="353d2-115">タスク</span><span class="sxs-lookup"><span data-stu-id="353d2-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="353d2-116">注釈</span><span class="sxs-lookup"><span data-stu-id="353d2-116">Remarks</span></span>

<span data-ttu-id="353d2-117">このプロパティを設定しない場合、既定値は FALSE と見なされます。</span><span class="sxs-lookup"><span data-stu-id="353d2-117">If this property is left unset, a default value of FALSE is assumed.</span></span> <span data-ttu-id="353d2-118">TRUE に設定されている場合は **、dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) および **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) プロパティも [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)で指定した値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="353d2-118">If it is set to TRUE, the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) and **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) properties must also be set as specified in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="353d2-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="353d2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="353d2-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="353d2-120">Protocol specifications</span></span>

<span data-ttu-id="353d2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="353d2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="353d2-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="353d2-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="353d2-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="353d2-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="353d2-124">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="353d2-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="353d2-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="353d2-125">Header files</span></span>

<span data-ttu-id="353d2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="353d2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="353d2-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="353d2-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="353d2-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="353d2-128">See also</span></span>



[<span data-ttu-id="353d2-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="353d2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="353d2-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="353d2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="353d2-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="353d2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="353d2-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="353d2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

