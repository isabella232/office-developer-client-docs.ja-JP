---
title: PidLidTaskAssigner 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigner
api_type:
- COM
ms.assetid: f7047e4e-0fb3-476b-9568-8f1135e6d970
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ef5f78fa36632227311d037ee61085c677920fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340090"
---
# <a name="pidlidtaskassigner-canonical-property"></a><span data-ttu-id="0d05e-103">PidLidTaskAssigner 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0d05e-103">PidLidTaskAssigner Canonical Property</span></span>

  
  
<span data-ttu-id="0d05e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d05e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="0d05e-105">タスクが最後に割り当てられたユーザーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d05e-105">Names the user who was last assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d05e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0d05e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d05e-107">dispidTaskDelegator</span><span class="sxs-lookup"><span data-stu-id="0d05e-107">dispidTaskDelegator</span></span>  <br/> |
|<span data-ttu-id="0d05e-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="0d05e-108">Property set:</span></span>  <br/> |<span data-ttu-id="0d05e-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0d05e-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0d05e-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0d05e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0d05e-111">0x00008121</span><span class="sxs-lookup"><span data-stu-id="0d05e-111">0x00008121</span></span>  <br/> |
|<span data-ttu-id="0d05e-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0d05e-112">Data type:</span></span>  <br/> |<span data-ttu-id="0d05e-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0d05e-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0d05e-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="0d05e-114">Area:</span></span>  <br/> |<span data-ttu-id="0d05e-115">タスク</span><span class="sxs-lookup"><span data-stu-id="0d05e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d05e-116">注釈</span><span class="sxs-lookup"><span data-stu-id="0d05e-116">Remarks</span></span>

<span data-ttu-id="0d05e-117">タスクが割り当てられていない場合、このプロパティは未設定の残りになります。</span><span class="sxs-lookup"><span data-stu-id="0d05e-117">If the task has not been assigned, this property is left unset.</span></span> <span data-ttu-id="0d05e-118">タスクの割り当て先がタスク要求を受け取った後、クライアントはこのプロパティを設定します。このプロパティはタスクの割り当て先のコピーでは設定されない。</span><span class="sxs-lookup"><span data-stu-id="0d05e-118">Because the client sets this property after the task assignee receives a task request, the property will not be set on the task assigner's copy of the task.</span></span> <span data-ttu-id="0d05e-119">クライアントが **dispidTaskMyDelegators** [(PidLidTaskAssigners)](pidlidtaskassigners-canonical-property.md)プロパティのタスク割り当て者リストにタスク割り当て者を追加または削除する場合は **、dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) プロパティを追加または削除したタスク割り当て者に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d05e-119">When the client adds or removes a task assigner from the task assigner list in the **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) property, the **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) property must be set to the added or removed task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0d05e-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0d05e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0d05e-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0d05e-121">Protocol specifications</span></span>

<span data-ttu-id="0d05e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d05e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d05e-123">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="0d05e-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0d05e-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d05e-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d05e-125">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="0d05e-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0d05e-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0d05e-126">Header files</span></span>

<span data-ttu-id="0d05e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d05e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d05e-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0d05e-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d05e-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d05e-129">See also</span></span>



[<span data-ttu-id="0d05e-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0d05e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d05e-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0d05e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d05e-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="0d05e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d05e-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="0d05e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

