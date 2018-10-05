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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399152"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="50287-103">PidLidTaskAcceptanceState 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="50287-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="50287-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50287-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50287-105">タスクの受け入れ状態を示します。</span><span class="sxs-lookup"><span data-stu-id="50287-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50287-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="50287-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50287-107">dispidTaskDelegValue</span><span class="sxs-lookup"><span data-stu-id="50287-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="50287-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="50287-108">Property set:</span></span>  <br/> |<span data-ttu-id="50287-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="50287-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="50287-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="50287-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="50287-111">0x0000812A</span><span class="sxs-lookup"><span data-stu-id="50287-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="50287-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="50287-112">Data type:</span></span>  <br/> |<span data-ttu-id="50287-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="50287-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="50287-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="50287-114">Area:</span></span>  <br/> |<span data-ttu-id="50287-115">タスク</span><span class="sxs-lookup"><span data-stu-id="50287-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50287-116">備考</span><span class="sxs-lookup"><span data-stu-id="50287-116">Remarks</span></span>

<span data-ttu-id="50287-117">次の表は、このプロパティの有効な値を示しています。</span><span class="sxs-lookup"><span data-stu-id="50287-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="50287-118">**値**</span><span class="sxs-lookup"><span data-stu-id="50287-118">**Value**</span></span>|<span data-ttu-id="50287-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="50287-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="50287-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50287-120">0x00000000</span></span>  <br/> |<span data-ttu-id="50287-121">タスクが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="50287-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="50287-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="50287-122">0x00000001</span></span>  <br/> |<span data-ttu-id="50287-123">タスクの受け入れ状況は不明です。</span><span class="sxs-lookup"><span data-stu-id="50287-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="50287-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="50287-124">0x00000002</span></span>  <br/> |<span data-ttu-id="50287-125">タスク実施者は、タスクを承諾しました。</span><span class="sxs-lookup"><span data-stu-id="50287-125">The task assignee accepted the task.</span></span> <span data-ttu-id="50287-126">クライアントは、タスクの承認を処理するとき、この値が設定されています。</span><span class="sxs-lookup"><span data-stu-id="50287-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="50287-127">0x00000003</span><span class="sxs-lookup"><span data-stu-id="50287-127">0x00000003</span></span>  <br/> |<span data-ttu-id="50287-128">タスク実施者は、タスクを拒否します。</span><span class="sxs-lookup"><span data-stu-id="50287-128">The task assignee rejected the task.</span></span> <span data-ttu-id="50287-129">クライアントは、タスクの辞退を処理するとき、この値が設定されています。</span><span class="sxs-lookup"><span data-stu-id="50287-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="50287-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="50287-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="50287-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="50287-131">Protocol specifications</span></span>

<span data-ttu-id="50287-132">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50287-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50287-133">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="50287-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="50287-134">[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50287-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50287-135">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="50287-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="50287-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="50287-136">Header files</span></span>

<span data-ttu-id="50287-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50287-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="50287-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="50287-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50287-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="50287-139">See also</span></span>



[<span data-ttu-id="50287-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="50287-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50287-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="50287-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50287-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="50287-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50287-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="50287-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

