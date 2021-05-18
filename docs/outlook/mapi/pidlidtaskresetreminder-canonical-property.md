---
title: PidLidTaskResetReminder 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskResetReminder
api_type:
- COM
ms.assetid: f6da69ff-a913-4a65-bb07-8ad3c5685e5e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a438fb2b1862d44905a63fda3e5f68b7878cd99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316619"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a><span data-ttu-id="182d5-103">PidLidTaskResetReminder 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="182d5-103">PidLidTaskResetReminder Canonical Property</span></span>

  
  
<span data-ttu-id="182d5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="182d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="182d5-105">**dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) が FALSE である場合でも、定期的なタスクの今後のインスタンスにリマインダーが必要かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="182d5-105">Indicates whether future instances of recurring tasks need reminders, even though **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) is FALSE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="182d5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="182d5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="182d5-107">dispidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="182d5-107">dispidTaskResetReminder</span></span>  <br/> |
|<span data-ttu-id="182d5-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="182d5-108">Property set:</span></span>  <br/> |<span data-ttu-id="182d5-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="182d5-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="182d5-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="182d5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="182d5-111">0x00008107</span><span class="sxs-lookup"><span data-stu-id="182d5-111">0x00008107</span></span>  <br/> |
|<span data-ttu-id="182d5-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="182d5-112">Data type:</span></span>  <br/> |<span data-ttu-id="182d5-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="182d5-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="182d5-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="182d5-114">Area:</span></span>  <br/> |<span data-ttu-id="182d5-115">タスク</span><span class="sxs-lookup"><span data-stu-id="182d5-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="182d5-116">注釈</span><span class="sxs-lookup"><span data-stu-id="182d5-116">Remarks</span></span>

<span data-ttu-id="182d5-117">この値は、タスクのアラームが閉じらされた場合は TRUE に設定され、それ以外の場合は FALSE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="182d5-117">This value is set to TRUE when the task's reminder is dismissed, and set to FALSE otherwise.</span></span> <span data-ttu-id="182d5-118">設定を解除した場合、既定の FALSE が使用されます。</span><span class="sxs-lookup"><span data-stu-id="182d5-118">If left unset, a default of FALSE is assumed.</span></span>
  
<span data-ttu-id="182d5-119">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)で指定されている通り **、dispidReminderSet** プロパティは、タスクにアラームが設定されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="182d5-119">As specified in [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), the **dispidReminderSet** property indicates whether a reminder is set on the task.</span></span> <span data-ttu-id="182d5-120">ただし、このプロパティは、1 つのタスクにアラームが存在するのみを示します。</span><span class="sxs-lookup"><span data-stu-id="182d5-120">However, this property only indicates the presence of a reminder on a single task.</span></span> <span data-ttu-id="182d5-121">定期的なタスクの将来のインスタンスにリマインダーが必要かどうかを判断するために単独で使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="182d5-121">It cannot be used alone to determine whether a future instance of a recurring task needs a reminder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="182d5-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="182d5-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="182d5-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="182d5-123">Protocol specifications</span></span>

<span data-ttu-id="182d5-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="182d5-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="182d5-125">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="182d5-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="182d5-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="182d5-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="182d5-127">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="182d5-127">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="182d5-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="182d5-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="182d5-129">メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="182d5-129">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="182d5-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="182d5-130">Header files</span></span>

<span data-ttu-id="182d5-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="182d5-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="182d5-132">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="182d5-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="182d5-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="182d5-133">See also</span></span>



[<span data-ttu-id="182d5-134">PidLidReminderSet ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="182d5-134">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)


[<span data-ttu-id="182d5-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="182d5-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="182d5-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="182d5-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="182d5-137">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="182d5-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="182d5-138">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="182d5-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

