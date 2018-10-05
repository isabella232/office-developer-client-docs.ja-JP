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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a438fb2b1862d44905a63fda3e5f68b7878cd99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384956"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a><span data-ttu-id="ae6da-103">PidLidTaskResetReminder 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ae6da-103">PidLidTaskResetReminder Canonical Property</span></span>

  
  
<span data-ttu-id="ae6da-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae6da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae6da-105">**DispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) が FALSE である場合でも、定期的な仕事の将来のインスタンスに通知が必要なかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ae6da-105">Indicates whether future instances of recurring tasks need reminders, even though **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) is FALSE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ae6da-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ae6da-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ae6da-107">dispidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="ae6da-107">dispidTaskResetReminder</span></span>  <br/> |
|<span data-ttu-id="ae6da-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="ae6da-108">Property set:</span></span>  <br/> |<span data-ttu-id="ae6da-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="ae6da-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="ae6da-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ae6da-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ae6da-111">0x00008107</span><span class="sxs-lookup"><span data-stu-id="ae6da-111">0x00008107</span></span>  <br/> |
|<span data-ttu-id="ae6da-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ae6da-112">Data type:</span></span>  <br/> |<span data-ttu-id="ae6da-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ae6da-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ae6da-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="ae6da-114">Area:</span></span>  <br/> |<span data-ttu-id="ae6da-115">タスク</span><span class="sxs-lookup"><span data-stu-id="ae6da-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae6da-116">備考</span><span class="sxs-lookup"><span data-stu-id="ae6da-116">Remarks</span></span>

<span data-ttu-id="ae6da-117">タスクのアラームを閉じる、およびそれ以外の場合は FALSE に設定すると、この値は TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="ae6da-117">This value is set to TRUE when the task's reminder is dismissed, and set to FALSE otherwise.</span></span> <span data-ttu-id="ae6da-118">未設定のままに、既定値は FALSE と見なされます。</span><span class="sxs-lookup"><span data-stu-id="ae6da-118">If left unset, a default of FALSE is assumed.</span></span>
  
<span data-ttu-id="ae6da-119">[[MS OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)で指定したとは、 **dispidReminderSet**プロパティは、タスクにアラームを設定するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ae6da-119">As specified in [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), the **dispidReminderSet** property indicates whether a reminder is set on the task.</span></span> <span data-ttu-id="ae6da-120">ただし、このプロパティには、1 つのタスクにアラームが存在することだけを示します。</span><span class="sxs-lookup"><span data-stu-id="ae6da-120">However, this property only indicates the presence of a reminder on a single task.</span></span> <span data-ttu-id="ae6da-121">アラームが定期的な仕事の将来のインスタンスに必要があるかどうかを確認するには、単独で使用できません。</span><span class="sxs-lookup"><span data-stu-id="ae6da-121">It cannot be used alone to determine whether a future instance of a recurring task needs a reminder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ae6da-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ae6da-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ae6da-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ae6da-123">Protocol specifications</span></span>

<span data-ttu-id="ae6da-124">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae6da-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ae6da-125">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ae6da-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ae6da-126">[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae6da-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ae6da-127">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="ae6da-127">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="ae6da-128">[[MS OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae6da-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ae6da-129">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="ae6da-129">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ae6da-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ae6da-130">Header files</span></span>

<span data-ttu-id="ae6da-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ae6da-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="ae6da-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ae6da-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ae6da-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae6da-133">See also</span></span>



[<span data-ttu-id="ae6da-134">PidLidReminderSet ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="ae6da-134">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)


[<span data-ttu-id="ae6da-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ae6da-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ae6da-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ae6da-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ae6da-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ae6da-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ae6da-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ae6da-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

