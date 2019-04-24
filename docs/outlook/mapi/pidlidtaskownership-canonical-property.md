---
title: PidLidTaskOwnership 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOwnership
api_type:
- COM
ms.assetid: 805dcb6c-f405-4c4d-8bca-af4bd9cd44fa
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 45fcba3f18aeb9092b71e28a6b68e42ad1abe77d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332110"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="38525-103">PidLidTaskOwnership 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="38525-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="38525-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38525-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38525-105">タスクに対する現在のユーザーの役割を示します。</span><span class="sxs-lookup"><span data-stu-id="38525-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38525-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="38525-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38525-107">dispidtaskownership 所有権</span><span class="sxs-lookup"><span data-stu-id="38525-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="38525-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="38525-108">Property set:</span></span>  <br/> |<span data-ttu-id="38525-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="38525-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="38525-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="38525-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="38525-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="38525-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="38525-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="38525-112">Data type:</span></span>  <br/> |<span data-ttu-id="38525-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="38525-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="38525-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="38525-114">Area:</span></span>  <br/> |<span data-ttu-id="38525-115">タスク</span><span class="sxs-lookup"><span data-stu-id="38525-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38525-116">解説</span><span class="sxs-lookup"><span data-stu-id="38525-116">Remarks</span></span>

<span data-ttu-id="38525-117">このプロパティには、次のいずれかの値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="38525-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="38525-118">**値**</span><span class="sxs-lookup"><span data-stu-id="38525-118">**Value**</span></span>|<span data-ttu-id="38525-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="38525-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="38525-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38525-120">0x00000000</span></span>  <br/> |<span data-ttu-id="38525-121">タスクが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="38525-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="38525-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="38525-122">0x00000001</span></span>  <br/> |<span data-ttu-id="38525-123">タスクは、タスク assigner のタスクのコピーです。</span><span class="sxs-lookup"><span data-stu-id="38525-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="38525-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="38525-124">0x00000002</span></span>  <br/> |<span data-ttu-id="38525-125">タスクは、タスクのタスク実施者のタスクのコピーです。</span><span class="sxs-lookup"><span data-stu-id="38525-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="38525-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="38525-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38525-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="38525-127">Protocol specifications</span></span>

<span data-ttu-id="38525-128">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38525-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38525-129">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="38525-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="38525-130">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38525-130">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38525-131">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="38525-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38525-132">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="38525-132">Header files</span></span>

<span data-ttu-id="38525-133">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38525-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="38525-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="38525-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38525-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="38525-135">See also</span></span>



[<span data-ttu-id="38525-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="38525-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38525-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="38525-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38525-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="38525-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38525-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="38525-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

