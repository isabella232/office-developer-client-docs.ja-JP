---
title: PidLidTaskLastUser 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUser
api_type:
- COM
ms.assetid: 914c55e9-cb36-46a4-b5ee-382413fa25f9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 76311a76001b122bdfd984b9dedc37c2ff878fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360446"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="2ddae-103">PidLidTaskLastUser 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ddae-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="2ddae-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ddae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ddae-105">タスクの所有者である最新のユーザーの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="2ddae-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ddae-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2ddae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ddae-107">dispidtasklastuser</span><span class="sxs-lookup"><span data-stu-id="2ddae-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="2ddae-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="2ddae-108">Property set:</span></span>  <br/> |<span data-ttu-id="2ddae-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="2ddae-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="2ddae-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="2ddae-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2ddae-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="2ddae-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="2ddae-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2ddae-112">Data type:</span></span>  <br/> |<span data-ttu-id="2ddae-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2ddae-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2ddae-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="2ddae-114">Area:</span></span>  <br/> |<span data-ttu-id="2ddae-115">タスク</span><span class="sxs-lookup"><span data-stu-id="2ddae-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ddae-116">解説</span><span class="sxs-lookup"><span data-stu-id="2ddae-116">Remarks</span></span>

<span data-ttu-id="2ddae-117">クライアントは、タスク要求を送信する前に、このプロパティをタスク assigner の名前に設定します。</span><span class="sxs-lookup"><span data-stu-id="2ddae-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="2ddae-118">クライアントは、タスクの承諾を送信する前に、タスクの割り当て先の名前にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2ddae-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="2ddae-119">クライアントがタスク拒否を送信する前に、このプロパティはタスク assigner の名前に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2ddae-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ddae-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2ddae-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ddae-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2ddae-121">Protocol specifications</span></span>

<span data-ttu-id="2ddae-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ddae-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ddae-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ddae-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2ddae-124">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ddae-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ddae-125">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="2ddae-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ddae-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="2ddae-126">Header files</span></span>

<span data-ttu-id="2ddae-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ddae-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ddae-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ddae-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ddae-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ddae-129">See also</span></span>



[<span data-ttu-id="2ddae-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2ddae-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ddae-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ddae-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ddae-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2ddae-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ddae-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2ddae-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

