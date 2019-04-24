---
title: PidLidTaskAssigners 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 97a4915d5422f6c5463ed399835172725b83407f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303067"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="a9333-103">PidLidTaskAssigners 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a9333-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="a9333-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9333-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9333-105">タスク assigners を表すエントリのスタックが格納されています。</span><span class="sxs-lookup"><span data-stu-id="a9333-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="a9333-106">最新のタスク assigner がスタックの一番上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a9333-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9333-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a9333-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9333-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="a9333-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="a9333-109">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="a9333-109">Property set:</span></span>  <br/> |<span data-ttu-id="a9333-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="a9333-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="a9333-111">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a9333-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a9333-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="a9333-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="a9333-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a9333-113">Data type:</span></span>  <br/> |<span data-ttu-id="a9333-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9333-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a9333-115">エリア:</span><span class="sxs-lookup"><span data-stu-id="a9333-115">Area:</span></span>  <br/> |<span data-ttu-id="a9333-116">タスク</span><span class="sxs-lookup"><span data-stu-id="a9333-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9333-117">解説</span><span class="sxs-lookup"><span data-stu-id="a9333-117">Remarks</span></span>

<span data-ttu-id="a9333-118">クライアントは、タスク要求を受信すると、このプロパティに追加されます。この構造は、タスクの送信者を表すエントリである[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)で定義されています。</span><span class="sxs-lookup"><span data-stu-id="a9333-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="a9333-119">クライアントがタスクの拒否を受信すると、クライアントはこのプロパティから最後のタスク assigner エントリを削除します。</span><span class="sxs-lookup"><span data-stu-id="a9333-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="a9333-120">クライアントは、タスク応答を送信すると、その応答をこのプロパティの値にリストされている最後のタスク assigner に送信します。</span><span class="sxs-lookup"><span data-stu-id="a9333-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a9333-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a9333-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a9333-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a9333-122">Protocol specifications</span></span>

<span data-ttu-id="a9333-123">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9333-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9333-124">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a9333-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a9333-125">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9333-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9333-126">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="a9333-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="a9333-127">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a9333-127">Header files</span></span>

<span data-ttu-id="a9333-128">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9333-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9333-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a9333-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9333-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9333-130">See also</span></span>



[<span data-ttu-id="a9333-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a9333-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9333-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a9333-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9333-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a9333-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9333-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a9333-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

