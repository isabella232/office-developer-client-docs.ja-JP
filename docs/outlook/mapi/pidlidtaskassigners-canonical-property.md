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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 97a4915d5422f6c5463ed399835172725b83407f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303067"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="b1588-103">PidLidTaskAssigners 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1588-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="b1588-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1588-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1588-105">タスク割り当て者を表すエントリのスタックが含まれる。</span><span class="sxs-lookup"><span data-stu-id="b1588-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="b1588-106">最新のタスク割り当て者がスタックの上部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b1588-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1588-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b1588-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1588-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="b1588-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="b1588-109">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="b1588-109">Property set:</span></span>  <br/> |<span data-ttu-id="b1588-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b1588-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b1588-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b1588-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b1588-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="b1588-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="b1588-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b1588-113">Data type:</span></span>  <br/> |<span data-ttu-id="b1588-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b1588-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b1588-115">エリア:</span><span class="sxs-lookup"><span data-stu-id="b1588-115">Area:</span></span>  <br/> |<span data-ttu-id="b1588-116">タスク</span><span class="sxs-lookup"><span data-stu-id="b1588-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1588-117">注釈</span><span class="sxs-lookup"><span data-stu-id="b1588-117">Remarks</span></span>

<span data-ttu-id="b1588-118">クライアントはタスク要求を受信すると、このプロパティに追加されます。このプロパティには、タスクの送信者を表すエントリである [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)で定義されている構造が追加されます。</span><span class="sxs-lookup"><span data-stu-id="b1588-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="b1588-119">クライアントがタスク拒否を受け取った場合、クライアントは最後のタスク割り当て者エントリをこのプロパティから削除します。</span><span class="sxs-lookup"><span data-stu-id="b1588-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="b1588-120">クライアントがタスク応答を送信すると、クライアントは、このプロパティの値にリストされている最後のタスク割り当て者に送信します。</span><span class="sxs-lookup"><span data-stu-id="b1588-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b1588-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b1588-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1588-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b1588-122">Protocol specifications</span></span>

<span data-ttu-id="b1588-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1588-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1588-124">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="b1588-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1588-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1588-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1588-126">タスク、タスクの割り当て、およびタスクの更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="b1588-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="b1588-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b1588-127">Header files</span></span>

<span data-ttu-id="b1588-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1588-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1588-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1588-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1588-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1588-130">See also</span></span>



[<span data-ttu-id="b1588-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b1588-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1588-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1588-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1588-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b1588-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1588-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b1588-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

