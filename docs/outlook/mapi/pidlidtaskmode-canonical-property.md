---
title: PidLidTaskMode 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d0ae319a6b5fa4c901ec7d318c7ebdd216a2adeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357940"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="5b9a5-103">PidLidTaskMode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5b9a5-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="5b9a5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b9a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b9a5-105">タスクの割り当ての状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b9a5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5b9a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b9a5-107">dispidtaskmode</span><span class="sxs-lookup"><span data-stu-id="5b9a5-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="5b9a5-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="5b9a5-108">Property set:</span></span>  <br/> |<span data-ttu-id="5b9a5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5b9a5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5b9a5-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5b9a5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5b9a5-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="5b9a5-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="5b9a5-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5b9a5-112">Data type:</span></span>  <br/> |<span data-ttu-id="5b9a5-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5b9a5-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5b9a5-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="5b9a5-114">Area:</span></span>  <br/> |<span data-ttu-id="5b9a5-115">タスク</span><span class="sxs-lookup"><span data-stu-id="5b9a5-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b9a5-116">解説</span><span class="sxs-lookup"><span data-stu-id="5b9a5-116">Remarks</span></span>

<span data-ttu-id="5b9a5-117">この値は、次のいずれかであることが必要です。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="5b9a5-118">**値**</span><span class="sxs-lookup"><span data-stu-id="5b9a5-118">**Value**</span></span>|<span data-ttu-id="5b9a5-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="5b9a5-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b9a5-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b9a5-120">0x00000000</span></span>  <br/> |<span data-ttu-id="5b9a5-121">タスクが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="5b9a5-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5b9a5-122">0x00000001</span></span>  <br/> |<span data-ttu-id="5b9a5-123">タスクは、タスクの依頼に埋め込まれています。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="5b9a5-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5b9a5-124">0x00000002</span></span>  <br/> |<span data-ttu-id="5b9a5-125">タスクは、タスクの実施者によって承諾されました。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="5b9a5-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="5b9a5-126">0x00000003</span></span>  <br/> |<span data-ttu-id="5b9a5-127">タスクは、タスクの実施者によって却下されました。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="5b9a5-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5b9a5-128">0x00000004</span></span>  <br/> |<span data-ttu-id="5b9a5-129">タスクは、タスクの更新に埋め込まれています。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="5b9a5-130">0x00000005</span><span class="sxs-lookup"><span data-stu-id="5b9a5-130">0x00000005</span></span>  <br/> |<span data-ttu-id="5b9a5-131">タスクは、タスク assigner に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5b9a5-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5b9a5-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b9a5-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5b9a5-133">Protocol specifications</span></span>

<span data-ttu-id="5b9a5-134">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b9a5-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b9a5-135">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5b9a5-136">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b9a5-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b9a5-137">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b9a5-138">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="5b9a5-138">Header files</span></span>

<span data-ttu-id="5b9a5-139">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b9a5-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b9a5-140">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b9a5-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="5b9a5-141">See also</span></span>



[<span data-ttu-id="5b9a5-142">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5b9a5-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b9a5-143">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5b9a5-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b9a5-144">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5b9a5-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b9a5-145">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5b9a5-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

