---
title: PidLidTaskMode の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f8eef7863cec565403d41dae26687b75f078e0d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802233"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="dc9ef-103">PidLidTaskMode の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="dc9ef-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="dc9ef-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc9ef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc9ef-105">タスクの割り当ての状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc9ef-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc9ef-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="dc9ef-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="dc9ef-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-108">Property set:</span></span>  <br/> |<span data-ttu-id="dc9ef-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="dc9ef-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="dc9ef-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="dc9ef-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dc9ef-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="dc9ef-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="dc9ef-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-112">Data type:</span></span>  <br/> |<span data-ttu-id="dc9ef-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dc9ef-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dc9ef-114">領域:</span><span class="sxs-lookup"><span data-stu-id="dc9ef-114">Area:</span></span>  <br/> |<span data-ttu-id="dc9ef-115">タスク</span><span class="sxs-lookup"><span data-stu-id="dc9ef-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc9ef-116">備考</span><span class="sxs-lookup"><span data-stu-id="dc9ef-116">Remarks</span></span>

<span data-ttu-id="dc9ef-117">値は、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="dc9ef-118">**値**</span><span class="sxs-lookup"><span data-stu-id="dc9ef-118">**Value**</span></span>|<span data-ttu-id="dc9ef-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="dc9ef-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc9ef-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc9ef-120">0x00000000</span></span>  <br/> |<span data-ttu-id="dc9ef-121">タスクが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="dc9ef-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dc9ef-122">0x00000001</span></span>  <br/> |<span data-ttu-id="dc9ef-123">タスクは、タスクの要求に埋め込まれます。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="dc9ef-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="dc9ef-124">0x00000002</span></span>  <br/> |<span data-ttu-id="dc9ef-125">タスクは、タスク実施者によって承認されました。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="dc9ef-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="dc9ef-126">0x00000003</span></span>  <br/> |<span data-ttu-id="dc9ef-127">タスクは、タスク実施者によって拒否されました。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="dc9ef-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="dc9ef-128">0x00000004</span></span>  <br/> |<span data-ttu-id="dc9ef-129">タスクは、タスクの更新に埋め込まれます。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="dc9ef-130">0x00000005</span><span class="sxs-lookup"><span data-stu-id="dc9ef-130">0x00000005</span></span>  <br/> |<span data-ttu-id="dc9ef-131">作業仕事を割り当てた人にタスクが割り当てられました。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="dc9ef-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="dc9ef-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dc9ef-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="dc9ef-133">Protocol specifications</span></span>

<span data-ttu-id="dc9ef-134">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc9ef-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc9ef-135">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dc9ef-136">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc9ef-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc9ef-137">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dc9ef-138">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="dc9ef-138">Header files</span></span>

<span data-ttu-id="dc9ef-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc9ef-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc9ef-140">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc9ef-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc9ef-141">See also</span></span>



[<span data-ttu-id="dc9ef-142">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="dc9ef-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc9ef-143">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="dc9ef-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc9ef-144">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="dc9ef-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc9ef-145">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="dc9ef-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

