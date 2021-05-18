---
title: PidLidTaskDeadOccurrence 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDeadOccurrence
api_type:
- COM
ms.assetid: e78287ff-f8cc-45ea-8da8-e7a7359e651c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0b740368aae43549e81cf3f4f6de40526c505b6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303431"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a><span data-ttu-id="b1b53-103">PidLidTaskDeadOccurrence 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1b53-103">PidLidTaskDeadOccurrence Canonical Property</span></span>

  
  
<span data-ttu-id="b1b53-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1b53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1b53-105">新しいオカレンスを生成する必要があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b1b53-105">Indicates whether new occurrences must be generated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1b53-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b1b53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1b53-107">dispidTaskDeadOccur</span><span class="sxs-lookup"><span data-stu-id="b1b53-107">dispidTaskDeadOccur</span></span>  <br/> |
|<span data-ttu-id="b1b53-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="b1b53-108">Property set:</span></span>  <br/> |<span data-ttu-id="b1b53-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b1b53-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b1b53-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b1b53-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b1b53-111">0x00008109</span><span class="sxs-lookup"><span data-stu-id="b1b53-111">0x00008109</span></span>  <br/> |
|<span data-ttu-id="b1b53-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b1b53-112">Data type:</span></span>  <br/> |<span data-ttu-id="b1b53-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b1b53-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b1b53-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="b1b53-114">Area:</span></span>  <br/> |<span data-ttu-id="b1b53-115">タスク</span><span class="sxs-lookup"><span data-stu-id="b1b53-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1b53-116">注釈</span><span class="sxs-lookup"><span data-stu-id="b1b53-116">Remarks</span></span>

<span data-ttu-id="b1b53-117">最後のインスタンスが過去に存在するか、指定した数のインスタンスが生成された場合、定期的なパターンは無効になります。</span><span class="sxs-lookup"><span data-stu-id="b1b53-117">A recurrence pattern is no longer in effect when its final instance is in the past or its specified number of instances has been generated.</span></span> <span data-ttu-id="b1b53-118">クライアントは、新しいタスクの場合は FALSE に、定期的なタスクの最後のインスタンスを生成する場合は TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="b1b53-118">The client sets this property to FALSE for a new task or to TRUE when it generates the last instance of a recurring task.</span></span> <span data-ttu-id="b1b53-119">タスクをコピーして新しいインスタンスを生成すると、このプロパティはコピーの TRUE に設定されます。これは完了したインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="b1b53-119">When you copy a task to generate a new instance, this property is set to TRUE on the copy, which is the completed instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b1b53-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b1b53-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1b53-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b1b53-121">Protocol specifications</span></span>

<span data-ttu-id="b1b53-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1b53-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1b53-123">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="b1b53-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1b53-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1b53-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1b53-125">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="b1b53-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="b1b53-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b1b53-126">Header files</span></span>

<span data-ttu-id="b1b53-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1b53-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1b53-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1b53-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1b53-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1b53-129">See also</span></span>



[<span data-ttu-id="b1b53-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b1b53-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1b53-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1b53-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1b53-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b1b53-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1b53-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b1b53-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

