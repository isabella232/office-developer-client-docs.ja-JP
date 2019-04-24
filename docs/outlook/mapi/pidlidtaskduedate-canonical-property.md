---
title: PidLidTaskDueDate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDueDate
api_type:
- COM
ms.assetid: 69ed3d48-3741-4a9a-8f98-51382b850c27
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2e21d164cbb9403d3fa1dc05cf474359a517d64b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303326"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="d1f51-103">PidLidTaskDueDate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d1f51-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="d1f51-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1f51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1f51-105">ユーザーがタスクを完了することを想定している日付を表します。</span><span class="sxs-lookup"><span data-stu-id="d1f51-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1f51-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d1f51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1f51-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="d1f51-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="d1f51-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="d1f51-108">Property set:</span></span>  <br/> |<span data-ttu-id="d1f51-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="d1f51-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="d1f51-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d1f51-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d1f51-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="d1f51-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="d1f51-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d1f51-112">Data type:</span></span>  <br/> |<span data-ttu-id="d1f51-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d1f51-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d1f51-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="d1f51-114">Area:</span></span>  <br/> |<span data-ttu-id="d1f51-115">タスク</span><span class="sxs-lookup"><span data-stu-id="d1f51-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1f51-116">解説</span><span class="sxs-lookup"><span data-stu-id="d1f51-116">Remarks</span></span>

<span data-ttu-id="d1f51-117">このプロパティが設定されていない場合、または 0x5AE980E0 (1525252320) に設定されている場合は、タスクに期限がありません。</span><span class="sxs-lookup"><span data-stu-id="d1f51-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="d1f51-118">ただし、期限が省略可能になるのは、 **dispidtaskstartdate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) プロパティに開始日が指定されていない場合のみです。</span><span class="sxs-lookup"><span data-stu-id="d1f51-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="d1f51-119">タスクに期限が設定されている場合は、値に午前0時の時間コンポーネントを指定し、 **dispidcommonend** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) プロパティも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1f51-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="d1f51-120">**dispidtaskstartdate**の開始日が設定されている場合、 **dispidTaskDueDate**プロパティの値は、 **dispidtaskstartdate**の値以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1f51-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d1f51-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d1f51-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1f51-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d1f51-122">Protocol specifications</span></span>

<span data-ttu-id="d1f51-123">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1f51-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1f51-124">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d1f51-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d1f51-125">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1f51-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1f51-126">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="d1f51-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="d1f51-127">[[OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1f51-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1f51-128">電子メールおよびその他のオブジェクトの事前通知のプロパティと相互作用モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="d1f51-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1f51-129">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="d1f51-129">Header files</span></span>

<span data-ttu-id="d1f51-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1f51-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1f51-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d1f51-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1f51-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1f51-132">See also</span></span>



[<span data-ttu-id="d1f51-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d1f51-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1f51-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d1f51-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1f51-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d1f51-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1f51-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d1f51-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

