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
ms.openlocfilehash: 94ec76d3247421f163775245c43ee68e6f9b560b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569086"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a><span data-ttu-id="269e0-103">PidLidTaskFRecurring 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="269e0-103">PidLidTaskFRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="269e0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="269e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="269e0-105">タスクが定期的なパターンを含めるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="269e0-105">Indicates whether the task includes a recurrence pattern.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="269e0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="269e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="269e0-107">dispidTaskFRecur</span><span class="sxs-lookup"><span data-stu-id="269e0-107">dispidTaskFRecur</span></span>  <br/> |
|<span data-ttu-id="269e0-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="269e0-108">Property set:</span></span>  <br/> |<span data-ttu-id="269e0-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="269e0-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="269e0-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="269e0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="269e0-111">0x00008126</span><span class="sxs-lookup"><span data-stu-id="269e0-111">0x00008126</span></span>  <br/> |
|<span data-ttu-id="269e0-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="269e0-112">Data type:</span></span>  <br/> |<span data-ttu-id="269e0-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="269e0-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="269e0-114">領域:</span><span class="sxs-lookup"><span data-stu-id="269e0-114">Area:</span></span>  <br/> |<span data-ttu-id="269e0-115">タスク</span><span class="sxs-lookup"><span data-stu-id="269e0-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="269e0-116">注釈</span><span class="sxs-lookup"><span data-stu-id="269e0-116">Remarks</span></span>

<span data-ttu-id="269e0-117">このプロパティが未設定のままには、FALSE の既定値が使われます。</span><span class="sxs-lookup"><span data-stu-id="269e0-117">If this property is left unset, a default value of FALSE is assumed.</span></span> <span data-ttu-id="269e0-118">として**dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) のプロパティを設定する必要があります**dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) は TRUE に設定されている場合は、 [[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)で指定します。</span><span class="sxs-lookup"><span data-stu-id="269e0-118">If it is set to TRUE, the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) and **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) properties must also be set as specified in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="269e0-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="269e0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="269e0-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="269e0-120">Protocol specifications</span></span>

<span data-ttu-id="269e0-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="269e0-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="269e0-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="269e0-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="269e0-123">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="269e0-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="269e0-124">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="269e0-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="269e0-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="269e0-125">Header files</span></span>

<span data-ttu-id="269e0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="269e0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="269e0-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="269e0-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="269e0-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="269e0-128">See also</span></span>



[<span data-ttu-id="269e0-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="269e0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="269e0-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="269e0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="269e0-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="269e0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="269e0-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="269e0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

