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
ms.openlocfilehash: 6b8ab295c9667d4cabb42c92dff7e8d1a3c2dd5e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584710"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="2a5b7-103">PidLidTaskDueDate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2a5b7-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="2a5b7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a5b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a5b7-105">ユーザーがタスクの完了に必要とする日付を表します。</span><span class="sxs-lookup"><span data-stu-id="2a5b7-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a5b7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2a5b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a5b7-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="2a5b7-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="2a5b7-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2a5b7-108">Property set:</span></span>  <br/> |<span data-ttu-id="2a5b7-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="2a5b7-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="2a5b7-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="2a5b7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2a5b7-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="2a5b7-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="2a5b7-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2a5b7-112">Data type:</span></span>  <br/> |<span data-ttu-id="2a5b7-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="2a5b7-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="2a5b7-114">領域:</span><span class="sxs-lookup"><span data-stu-id="2a5b7-114">Area:</span></span>  <br/> |<span data-ttu-id="2a5b7-115">タスク</span><span class="sxs-lookup"><span data-stu-id="2a5b7-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a5b7-116">注釈</span><span class="sxs-lookup"><span data-stu-id="2a5b7-116">Remarks</span></span>

<span data-ttu-id="2a5b7-117">このプロパティが未設定またはに設定の 0x5AE980E0 (1,525,252,320) である場合、タスクの締め切り日はありません。</span><span class="sxs-lookup"><span data-stu-id="2a5b7-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="2a5b7-118">ただし、 **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) のプロパティの開始日が指定されていない場合にだけは、期日はオプションです。</span><span class="sxs-lookup"><span data-stu-id="2a5b7-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="2a5b7-119">タスクに期限がある場合は、値が午前 0 時という時刻成分を持つ必要があり、 **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) のプロパティを設定する必要がありますもします。</span><span class="sxs-lookup"><span data-stu-id="2a5b7-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="2a5b7-120">**DispidTaskStartDate**に開始日が設定されている場合、 **dispidTaskDueDate**プロパティの値を必要があります**dispidTaskStartDate**の値以上です。</span><span class="sxs-lookup"><span data-stu-id="2a5b7-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2a5b7-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2a5b7-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2a5b7-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2a5b7-122">Protocol specifications</span></span>

<span data-ttu-id="2a5b7-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a5b7-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a5b7-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2a5b7-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2a5b7-125">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a5b7-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a5b7-126">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="2a5b7-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="2a5b7-127">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a5b7-127">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a5b7-128">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="2a5b7-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2a5b7-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2a5b7-129">Header files</span></span>

<span data-ttu-id="2a5b7-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a5b7-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a5b7-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2a5b7-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a5b7-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a5b7-132">See also</span></span>



[<span data-ttu-id="2a5b7-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2a5b7-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a5b7-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2a5b7-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a5b7-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2a5b7-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a5b7-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2a5b7-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

