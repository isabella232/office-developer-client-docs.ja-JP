---
title: PidLidTaskLastDelegate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastDelegate
api_type:
- COM
ms.assetid: 5eb8c1ce-063f-4273-acba-e6f9c994e7d3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ddf4b81ed35f500dad0029ea6375e9a75a996186
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355672"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="0680b-103">PidLidTaskLastDelegate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0680b-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="0680b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0680b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="0680b-105">タスクを最後に割り当てたユーザーまたは割り当てられたユーザーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="0680b-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0680b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0680b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0680b-107">dispidtasklastdelegate</span><span class="sxs-lookup"><span data-stu-id="0680b-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="0680b-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="0680b-108">Property set:</span></span>  <br/> |<span data-ttu-id="0680b-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0680b-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0680b-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0680b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0680b-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="0680b-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="0680b-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0680b-112">Data type:</span></span>  <br/> |<span data-ttu-id="0680b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0680b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0680b-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="0680b-114">Area:</span></span>  <br/> |<span data-ttu-id="0680b-115">タスク</span><span class="sxs-lookup"><span data-stu-id="0680b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0680b-116">解説</span><span class="sxs-lookup"><span data-stu-id="0680b-116">Remarks</span></span>

<span data-ttu-id="0680b-117">タスクの要求を送信する前に、クライアントはこのプロパティをタスク assigner の名前に設定します。</span><span class="sxs-lookup"><span data-stu-id="0680b-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="0680b-118">タスクの応答を送信する前に、クライアントはこのプロパティをタスクの実施者の名前に設定します。</span><span class="sxs-lookup"><span data-stu-id="0680b-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0680b-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0680b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0680b-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0680b-120">Protocol specifications</span></span>

<span data-ttu-id="0680b-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0680b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0680b-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0680b-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0680b-123">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0680b-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0680b-124">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="0680b-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0680b-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="0680b-125">Header files</span></span>

<span data-ttu-id="0680b-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0680b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0680b-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0680b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0680b-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="0680b-128">See also</span></span>



[<span data-ttu-id="0680b-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0680b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0680b-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0680b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0680b-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0680b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0680b-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0680b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

