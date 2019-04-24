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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ef5f78fa36632227311d037ee61085c677920fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340090"
---
# <a name="pidlidtaskassigner-canonical-property"></a><span data-ttu-id="58278-103">PidLidTaskAssigner 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="58278-103">PidLidTaskAssigner Canonical Property</span></span>

  
  
<span data-ttu-id="58278-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58278-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="58278-105">最後にタスクを割り当てたユーザーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="58278-105">Names the user who was last assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58278-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="58278-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58278-107">dispidTaskDelegator</span><span class="sxs-lookup"><span data-stu-id="58278-107">dispidTaskDelegator</span></span>  <br/> |
|<span data-ttu-id="58278-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="58278-108">Property set:</span></span>  <br/> |<span data-ttu-id="58278-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="58278-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="58278-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="58278-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="58278-111">0x00008121</span><span class="sxs-lookup"><span data-stu-id="58278-111">0x00008121</span></span>  <br/> |
|<span data-ttu-id="58278-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="58278-112">Data type:</span></span>  <br/> |<span data-ttu-id="58278-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="58278-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="58278-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="58278-114">Area:</span></span>  <br/> |<span data-ttu-id="58278-115">タスク</span><span class="sxs-lookup"><span data-stu-id="58278-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58278-116">解説</span><span class="sxs-lookup"><span data-stu-id="58278-116">Remarks</span></span>

<span data-ttu-id="58278-117">タスクが割り当てられていない場合、このプロパティは未設定のままになります。</span><span class="sxs-lookup"><span data-stu-id="58278-117">If the task has not been assigned, this property is left unset.</span></span> <span data-ttu-id="58278-118">タスクの担当者がタスクの依頼を受信した後、クライアントはこのプロパティを設定するため、このプロパティはタスク assigner のタスクのコピーには設定されません。</span><span class="sxs-lookup"><span data-stu-id="58278-118">Because the client sets this property after the task assignee receives a task request, the property will not be set on the task assigner's copy of the task.</span></span> <span data-ttu-id="58278-119">クライアントが**dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) プロパティのタスク assigner リストからタスク assigner を追加または削除する場合は、 **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) プロパティを追加されたに設定する必要があります。タスク assigner を削除しました。</span><span class="sxs-lookup"><span data-stu-id="58278-119">When the client adds or removes a task assigner from the task assigner list in the **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) property, the **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) property must be set to the added or removed task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="58278-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="58278-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58278-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="58278-121">Protocol specifications</span></span>

<span data-ttu-id="58278-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58278-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58278-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="58278-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58278-124">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58278-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58278-125">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="58278-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58278-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="58278-126">Header files</span></span>

<span data-ttu-id="58278-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58278-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="58278-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="58278-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58278-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="58278-129">See also</span></span>



[<span data-ttu-id="58278-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="58278-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58278-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="58278-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58278-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="58278-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58278-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="58278-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

