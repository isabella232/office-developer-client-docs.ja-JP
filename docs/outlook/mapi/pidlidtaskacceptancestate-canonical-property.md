---
title: PidLidTaskAcceptanceState 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b42be4b42d085aba8999a8c3f1a780ed972fa136
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331291"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="bdb98-103">PidLidTaskAcceptanceState 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bdb98-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="bdb98-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdb98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdb98-105">タスクの承認状態を示します。</span><span class="sxs-lookup"><span data-stu-id="bdb98-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bdb98-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bdb98-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bdb98-107">dispidTaskDelegValue</span><span class="sxs-lookup"><span data-stu-id="bdb98-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="bdb98-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="bdb98-108">Property set:</span></span>  <br/> |<span data-ttu-id="bdb98-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="bdb98-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="bdb98-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bdb98-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bdb98-111">0x0000812a</span><span class="sxs-lookup"><span data-stu-id="bdb98-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="bdb98-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bdb98-112">Data type:</span></span>  <br/> |<span data-ttu-id="bdb98-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bdb98-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bdb98-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="bdb98-114">Area:</span></span>  <br/> |<span data-ttu-id="bdb98-115">タスク</span><span class="sxs-lookup"><span data-stu-id="bdb98-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdb98-116">解説</span><span class="sxs-lookup"><span data-stu-id="bdb98-116">Remarks</span></span>

<span data-ttu-id="bdb98-117">次の表に、このプロパティに指定できる値を示します。</span><span class="sxs-lookup"><span data-stu-id="bdb98-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="bdb98-118">**値**</span><span class="sxs-lookup"><span data-stu-id="bdb98-118">**Value**</span></span>|<span data-ttu-id="bdb98-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="bdb98-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bdb98-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdb98-120">0x00000000</span></span>  <br/> |<span data-ttu-id="bdb98-121">タスクが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="bdb98-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="bdb98-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bdb98-122">0x00000001</span></span>  <br/> |<span data-ttu-id="bdb98-123">タスクの承諾状態が不明です。</span><span class="sxs-lookup"><span data-stu-id="bdb98-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="bdb98-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="bdb98-124">0x00000002</span></span>  <br/> |<span data-ttu-id="bdb98-125">タスクの実施者がタスクを承諾しました。</span><span class="sxs-lookup"><span data-stu-id="bdb98-125">The task assignee accepted the task.</span></span> <span data-ttu-id="bdb98-126">この値は、クライアントがタスクの承諾を処理するときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="bdb98-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="bdb98-127">0x00000003</span><span class="sxs-lookup"><span data-stu-id="bdb98-127">0x00000003</span></span>  <br/> |<span data-ttu-id="bdb98-128">タスクの実施者がタスクを拒否しました。</span><span class="sxs-lookup"><span data-stu-id="bdb98-128">The task assignee rejected the task.</span></span> <span data-ttu-id="bdb98-129">この値は、クライアントがタスクの却下を処理するときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="bdb98-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bdb98-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bdb98-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bdb98-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bdb98-131">Protocol specifications</span></span>

<span data-ttu-id="bdb98-132">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bdb98-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bdb98-133">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="bdb98-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bdb98-134">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bdb98-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bdb98-135">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="bdb98-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bdb98-136">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="bdb98-136">Header files</span></span>

<span data-ttu-id="bdb98-137">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bdb98-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="bdb98-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bdb98-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bdb98-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="bdb98-139">See also</span></span>



[<span data-ttu-id="bdb98-140">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bdb98-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bdb98-141">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bdb98-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bdb98-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bdb98-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bdb98-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bdb98-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

