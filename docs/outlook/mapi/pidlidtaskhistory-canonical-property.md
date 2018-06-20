---
title: PidLidTaskHistory の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6e53d91a80d7e3b3bb4bf02ff3446eb385293c6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802228"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="2f4df-103">PidLidTaskHistory の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="2f4df-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="2f4df-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2f4df-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2f4df-105">タスクを最後に加えられた変更の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="2f4df-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f4df-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="2f4df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2f4df-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="2f4df-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="2f4df-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2f4df-108">Property set:</span></span>  <br/> |<span data-ttu-id="2f4df-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="2f4df-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="2f4df-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="2f4df-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2f4df-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="2f4df-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="2f4df-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="2f4df-112">Data type:</span></span>  <br/> |<span data-ttu-id="2f4df-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2f4df-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2f4df-114">領域:</span><span class="sxs-lookup"><span data-stu-id="2f4df-114">Area:</span></span>  <br/> |<span data-ttu-id="2f4df-115">タスク</span><span class="sxs-lookup"><span data-stu-id="2f4df-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f4df-116">備考</span><span class="sxs-lookup"><span data-stu-id="2f4df-116">Remarks</span></span>

<span data-ttu-id="2f4df-117">このプロパティの値を設定すると、 **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) のプロパティは現在の時刻にも設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2f4df-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="2f4df-118">次の表は、 **dispidTaskHistory**プロパティの値を優先度順に一覧表示を示しています。</span><span class="sxs-lookup"><span data-stu-id="2f4df-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="2f4df-119">**値**</span><span class="sxs-lookup"><span data-stu-id="2f4df-119">**Value**</span></span>|<span data-ttu-id="2f4df-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="2f4df-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f4df-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2f4df-121">0x00000004</span></span>  <br/> |<span data-ttu-id="2f4df-122">**DispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) のプロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="2f4df-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="2f4df-123">0x00000003</span><span class="sxs-lookup"><span data-stu-id="2f4df-123">0x00000003</span></span>  <br/> |<span data-ttu-id="2f4df-124">別のプロパティが変更されました。</span><span class="sxs-lookup"><span data-stu-id="2f4df-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="2f4df-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2f4df-125">0x00000001</span></span>  <br/> |<span data-ttu-id="2f4df-126">タスク実施者は、このタスクを承諾します。</span><span class="sxs-lookup"><span data-stu-id="2f4df-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="2f4df-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2f4df-127">0x00000002</span></span>  <br/> |<span data-ttu-id="2f4df-128">タスク実施者は、このタスクを拒否します。</span><span class="sxs-lookup"><span data-stu-id="2f4df-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="2f4df-129">0x00000005</span><span class="sxs-lookup"><span data-stu-id="2f4df-129">0x00000005</span></span>  <br/> |<span data-ttu-id="2f4df-130">タスクは、タスクの実施者に割り当てられました。</span><span class="sxs-lookup"><span data-stu-id="2f4df-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="2f4df-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f4df-131">0x00000000</span></span>  <br/> |<span data-ttu-id="2f4df-132">変更は行われませんでした。</span><span class="sxs-lookup"><span data-stu-id="2f4df-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2f4df-133">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2f4df-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2f4df-134">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2f4df-134">Protocol specifications</span></span>

<span data-ttu-id="2f4df-135">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f4df-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f4df-136">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2f4df-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2f4df-137">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f4df-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f4df-138">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="2f4df-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2f4df-139">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2f4df-139">Header files</span></span>

<span data-ttu-id="2f4df-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f4df-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="2f4df-141">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2f4df-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f4df-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f4df-142">See also</span></span>



[<span data-ttu-id="2f4df-143">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2f4df-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2f4df-144">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2f4df-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2f4df-145">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="2f4df-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2f4df-146">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="2f4df-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

