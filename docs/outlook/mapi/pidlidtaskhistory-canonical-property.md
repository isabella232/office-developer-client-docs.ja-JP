---
title: PidLidTaskHistory 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303011"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="0c82c-103">PidLidTaskHistory 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c82c-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="0c82c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c82c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c82c-105">タスクに対して最後に行った変更の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="0c82c-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c82c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0c82c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c82c-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="0c82c-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="0c82c-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="0c82c-108">Property set:</span></span>  <br/> |<span data-ttu-id="0c82c-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0c82c-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0c82c-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0c82c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0c82c-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="0c82c-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="0c82c-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0c82c-112">Data type:</span></span>  <br/> |<span data-ttu-id="0c82c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0c82c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0c82c-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="0c82c-114">Area:</span></span>  <br/> |<span data-ttu-id="0c82c-115">タスク</span><span class="sxs-lookup"><span data-stu-id="0c82c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c82c-116">解説</span><span class="sxs-lookup"><span data-stu-id="0c82c-116">Remarks</span></span>

<span data-ttu-id="0c82c-117">このプロパティの値が設定されている場合は、 **dispidtasklastupdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) プロパティも現在の時刻に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c82c-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="0c82c-118">次の表に、 **dispidTaskHistory**プロパティの値を、優先度の高い順に示します。</span><span class="sxs-lookup"><span data-stu-id="0c82c-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="0c82c-119">**値**</span><span class="sxs-lookup"><span data-stu-id="0c82c-119">**Value**</span></span>|<span data-ttu-id="0c82c-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="0c82c-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0c82c-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="0c82c-121">0x00000004</span></span>  <br/> |<span data-ttu-id="0c82c-122">**dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) プロパティが変更されました。</span><span class="sxs-lookup"><span data-stu-id="0c82c-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="0c82c-123">0x00000003</span><span class="sxs-lookup"><span data-stu-id="0c82c-123">0x00000003</span></span>  <br/> |<span data-ttu-id="0c82c-124">別のプロパティが変更されました。</span><span class="sxs-lookup"><span data-stu-id="0c82c-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="0c82c-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0c82c-125">0x00000001</span></span>  <br/> |<span data-ttu-id="0c82c-126">タスクの実施者がこのタスクを承諾しました。</span><span class="sxs-lookup"><span data-stu-id="0c82c-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="0c82c-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0c82c-127">0x00000002</span></span>  <br/> |<span data-ttu-id="0c82c-128">タスクの実施者がこのタスクを拒否しました。</span><span class="sxs-lookup"><span data-stu-id="0c82c-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="0c82c-129">0x00000005</span><span class="sxs-lookup"><span data-stu-id="0c82c-129">0x00000005</span></span>  <br/> |<span data-ttu-id="0c82c-130">タスクは、タスクの担当者に割り当てられました。</span><span class="sxs-lookup"><span data-stu-id="0c82c-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="0c82c-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c82c-131">0x00000000</span></span>  <br/> |<span data-ttu-id="0c82c-132">変更は行われませんでした。</span><span class="sxs-lookup"><span data-stu-id="0c82c-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0c82c-133">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0c82c-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0c82c-134">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0c82c-134">Protocol specifications</span></span>

<span data-ttu-id="0c82c-135">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c82c-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c82c-136">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0c82c-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0c82c-137">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c82c-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c82c-138">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="0c82c-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0c82c-139">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="0c82c-139">Header files</span></span>

<span data-ttu-id="0c82c-140">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c82c-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c82c-141">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0c82c-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c82c-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c82c-142">See also</span></span>



[<span data-ttu-id="0c82c-143">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0c82c-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c82c-144">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c82c-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c82c-145">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0c82c-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c82c-146">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0c82c-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

