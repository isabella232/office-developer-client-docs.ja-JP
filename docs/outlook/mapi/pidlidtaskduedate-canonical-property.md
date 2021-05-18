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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2e21d164cbb9403d3fa1dc05cf474359a517d64b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303326"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="c9d5d-103">PidLidTaskDueDate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c9d5d-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="c9d5d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9d5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9d5d-105">ユーザーがタスクを完了する予定の日付を表します。</span><span class="sxs-lookup"><span data-stu-id="c9d5d-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9d5d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c9d5d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9d5d-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="c9d5d-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="c9d5d-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="c9d5d-108">Property set:</span></span>  <br/> |<span data-ttu-id="c9d5d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="c9d5d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="c9d5d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c9d5d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c9d5d-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="c9d5d-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="c9d5d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c9d5d-112">Data type:</span></span>  <br/> |<span data-ttu-id="c9d5d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c9d5d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c9d5d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="c9d5d-114">Area:</span></span>  <br/> |<span data-ttu-id="c9d5d-115">タスク</span><span class="sxs-lookup"><span data-stu-id="c9d5d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9d5d-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c9d5d-116">Remarks</span></span>

<span data-ttu-id="c9d5d-117">このプロパティの設定が解除または設定されている場合、タスクに期限はありません (1,525,252,320 0x5AE980E0)</span><span class="sxs-lookup"><span data-stu-id="c9d5d-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="c9d5d-118">ただし、期限は **、dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) プロパティに開始日が指定されている場合にのみ省略できます。</span><span class="sxs-lookup"><span data-stu-id="c9d5d-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="c9d5d-119">タスクに期日がある場合、値には午前 0 時の時刻コンポーネントが必要で **、dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) プロパティも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9d5d-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="c9d5d-120">**dispidTaskStartDate** に開始日がある場合 **、dispidTaskDueDate** プロパティの値は **、dispidTaskStartDate** の値以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9d5d-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c9d5d-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c9d5d-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c9d5d-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c9d5d-122">Protocol specifications</span></span>

<span data-ttu-id="c9d5d-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9d5d-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9d5d-124">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="c9d5d-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c9d5d-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9d5d-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9d5d-126">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="c9d5d-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="c9d5d-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9d5d-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9d5d-128">メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="c9d5d-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c9d5d-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c9d5d-129">Header files</span></span>

<span data-ttu-id="c9d5d-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9d5d-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9d5d-131">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c9d5d-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9d5d-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="c9d5d-132">See also</span></span>



[<span data-ttu-id="c9d5d-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c9d5d-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9d5d-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c9d5d-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9d5d-135">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c9d5d-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9d5d-136">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c9d5d-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

