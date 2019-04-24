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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aec9dd328e802e185c870d3ecd94cbd1d10ac67d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303053"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a><span data-ttu-id="d8309-103">PidLidTaskFRecurring 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d8309-103">PidLidTaskFRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="d8309-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8309-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8309-105">タスクに定期的なパターンを含めるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d8309-105">Indicates whether the task includes a recurrence pattern.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8309-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d8309-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d8309-107">dispidtaskfrecur</span><span class="sxs-lookup"><span data-stu-id="d8309-107">dispidTaskFRecur</span></span>  <br/> |
|<span data-ttu-id="d8309-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="d8309-108">Property set:</span></span>  <br/> |<span data-ttu-id="d8309-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="d8309-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="d8309-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d8309-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d8309-111">0x00008126</span><span class="sxs-lookup"><span data-stu-id="d8309-111">0x00008126</span></span>  <br/> |
|<span data-ttu-id="d8309-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d8309-112">Data type:</span></span>  <br/> |<span data-ttu-id="d8309-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d8309-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d8309-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="d8309-114">Area:</span></span>  <br/> |<span data-ttu-id="d8309-115">タスク</span><span class="sxs-lookup"><span data-stu-id="d8309-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8309-116">解説</span><span class="sxs-lookup"><span data-stu-id="d8309-116">Remarks</span></span>

<span data-ttu-id="d8309-117">このプロパティを未設定のままにした場合は、既定値の FALSE が想定されます。</span><span class="sxs-lookup"><span data-stu-id="d8309-117">If this property is left unset, a default value of FALSE is assumed.</span></span> <span data-ttu-id="d8309-118">このプロパティが TRUE に設定されている場合は、 **dispidtaskrecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) および**dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) の各プロパティも、 [[]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)で指定されているとおりに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8309-118">If it is set to TRUE, the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) and **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) properties must also be set as specified in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d8309-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d8309-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d8309-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d8309-120">Protocol specifications</span></span>

<span data-ttu-id="d8309-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8309-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8309-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d8309-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d8309-123">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8309-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8309-124">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="d8309-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d8309-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="d8309-125">Header files</span></span>

<span data-ttu-id="d8309-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d8309-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d8309-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d8309-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8309-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8309-128">See also</span></span>



[<span data-ttu-id="d8309-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d8309-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d8309-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d8309-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d8309-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d8309-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d8309-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d8309-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

