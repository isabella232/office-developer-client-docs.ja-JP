---
title: PidLidTaskAcceptanceState の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 970fc57a3fd129f0ac50af3f71e0d5e15ff22371
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802190"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="7bb4f-103">PidLidTaskAcceptanceState の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7bb4f-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="7bb4f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7bb4f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7bb4f-105">タスクの受け入れ状態を示します。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7bb4f-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7bb4f-107">dispidTaskDelegValue</span><span class="sxs-lookup"><span data-stu-id="7bb4f-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="7bb4f-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-108">Property set:</span></span>  <br/> |<span data-ttu-id="7bb4f-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="7bb4f-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="7bb4f-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7bb4f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7bb4f-111">0x0000812A</span><span class="sxs-lookup"><span data-stu-id="7bb4f-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="7bb4f-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-112">Data type:</span></span>  <br/> |<span data-ttu-id="7bb4f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7bb4f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7bb4f-114">領域:</span><span class="sxs-lookup"><span data-stu-id="7bb4f-114">Area:</span></span>  <br/> |<span data-ttu-id="7bb4f-115">タスク</span><span class="sxs-lookup"><span data-stu-id="7bb4f-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bb4f-116">備考</span><span class="sxs-lookup"><span data-stu-id="7bb4f-116">Remarks</span></span>

<span data-ttu-id="7bb4f-117">次の表は、このプロパティの有効な値を示しています。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="7bb4f-118">**値**</span><span class="sxs-lookup"><span data-stu-id="7bb4f-118">**Value**</span></span>|<span data-ttu-id="7bb4f-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="7bb4f-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7bb4f-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bb4f-120">0x00000000</span></span>  <br/> |<span data-ttu-id="7bb4f-121">タスクが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="7bb4f-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7bb4f-122">0x00000001</span></span>  <br/> |<span data-ttu-id="7bb4f-123">タスクの受け入れ状況は不明です。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="7bb4f-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7bb4f-124">0x00000002</span></span>  <br/> |<span data-ttu-id="7bb4f-125">タスク実施者は、タスクを承諾しました。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-125">The task assignee accepted the task.</span></span> <span data-ttu-id="7bb4f-126">クライアントは、タスクの承認を処理するとき、この値が設定されています。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="7bb4f-127">0x00000003</span><span class="sxs-lookup"><span data-stu-id="7bb4f-127">0x00000003</span></span>  <br/> |<span data-ttu-id="7bb4f-128">タスク実施者は、タスクを拒否します。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-128">The task assignee rejected the task.</span></span> <span data-ttu-id="7bb4f-129">クライアントは、タスクの辞退を処理するとき、この値が設定されています。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7bb4f-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7bb4f-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7bb4f-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7bb4f-131">Protocol specifications</span></span>

<span data-ttu-id="7bb4f-132">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7bb4f-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7bb4f-133">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7bb4f-134">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7bb4f-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7bb4f-135">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7bb4f-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7bb4f-136">Header files</span></span>

<span data-ttu-id="7bb4f-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7bb4f-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="7bb4f-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7bb4f-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="7bb4f-139">See also</span></span>



[<span data-ttu-id="7bb4f-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7bb4f-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7bb4f-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7bb4f-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7bb4f-142">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7bb4f-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7bb4f-143">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="7bb4f-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

