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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d0ae319a6b5fa4c901ec7d318c7ebdd216a2adeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357940"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="1bc61-103">PidLidTaskMode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1bc61-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="1bc61-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bc61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bc61-105">タスクの割り当て状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="1bc61-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1bc61-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1bc61-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1bc61-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="1bc61-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="1bc61-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="1bc61-108">Property set:</span></span>  <br/> |<span data-ttu-id="1bc61-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="1bc61-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="1bc61-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1bc61-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1bc61-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="1bc61-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="1bc61-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1bc61-112">Data type:</span></span>  <br/> |<span data-ttu-id="1bc61-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1bc61-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1bc61-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="1bc61-114">Area:</span></span>  <br/> |<span data-ttu-id="1bc61-115">タスク</span><span class="sxs-lookup"><span data-stu-id="1bc61-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bc61-116">注釈</span><span class="sxs-lookup"><span data-stu-id="1bc61-116">Remarks</span></span>

<span data-ttu-id="1bc61-117">値は、次のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bc61-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="1bc61-118">**値**</span><span class="sxs-lookup"><span data-stu-id="1bc61-118">**Value**</span></span>|<span data-ttu-id="1bc61-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="1bc61-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1bc61-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1bc61-120">0x00000000</span></span>  <br/> |<span data-ttu-id="1bc61-121">タスクが割り当てられていない。</span><span class="sxs-lookup"><span data-stu-id="1bc61-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="1bc61-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1bc61-122">0x00000001</span></span>  <br/> |<span data-ttu-id="1bc61-123">タスクはタスク要求に埋め込まれている。</span><span class="sxs-lookup"><span data-stu-id="1bc61-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="1bc61-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1bc61-124">0x00000002</span></span>  <br/> |<span data-ttu-id="1bc61-125">タスクは、タスクの割り当て先によって受け入れされました。</span><span class="sxs-lookup"><span data-stu-id="1bc61-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="1bc61-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="1bc61-126">0x00000003</span></span>  <br/> |<span data-ttu-id="1bc61-127">タスクは、タスクの割り当て先によって拒否されました。</span><span class="sxs-lookup"><span data-stu-id="1bc61-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="1bc61-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1bc61-128">0x00000004</span></span>  <br/> |<span data-ttu-id="1bc61-129">タスクはタスク更新プログラムに埋め込まれている。</span><span class="sxs-lookup"><span data-stu-id="1bc61-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="1bc61-130">0x00000005</span><span class="sxs-lookup"><span data-stu-id="1bc61-130">0x00000005</span></span>  <br/> |<span data-ttu-id="1bc61-131">タスクがタスク割り当て人に割り当て済みです。</span><span class="sxs-lookup"><span data-stu-id="1bc61-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1bc61-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1bc61-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1bc61-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1bc61-133">Protocol specifications</span></span>

<span data-ttu-id="1bc61-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1bc61-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1bc61-135">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="1bc61-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1bc61-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1bc61-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1bc61-137">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="1bc61-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1bc61-138">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1bc61-138">Header files</span></span>

<span data-ttu-id="1bc61-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1bc61-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="1bc61-140">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1bc61-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1bc61-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="1bc61-141">See also</span></span>



[<span data-ttu-id="1bc61-142">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1bc61-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1bc61-143">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1bc61-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1bc61-144">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="1bc61-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1bc61-145">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="1bc61-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

