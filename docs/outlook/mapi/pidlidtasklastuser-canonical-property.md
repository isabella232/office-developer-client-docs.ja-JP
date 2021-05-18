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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 76311a76001b122bdfd984b9dedc37c2ff878fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360446"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="c44ee-103">PidLidTaskLastUser 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c44ee-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="c44ee-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c44ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c44ee-105">タスクの所有者だった最新のユーザーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="c44ee-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c44ee-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c44ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c44ee-107">dispidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="c44ee-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="c44ee-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="c44ee-108">Property set:</span></span>  <br/> |<span data-ttu-id="c44ee-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="c44ee-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="c44ee-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c44ee-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c44ee-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="c44ee-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="c44ee-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c44ee-112">Data type:</span></span>  <br/> |<span data-ttu-id="c44ee-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c44ee-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c44ee-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="c44ee-114">Area:</span></span>  <br/> |<span data-ttu-id="c44ee-115">タスク</span><span class="sxs-lookup"><span data-stu-id="c44ee-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c44ee-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c44ee-116">Remarks</span></span>

<span data-ttu-id="c44ee-117">クライアントがタスク要求を送信する前に、このプロパティをタスク割り当て者の名前に設定します。</span><span class="sxs-lookup"><span data-stu-id="c44ee-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="c44ee-118">クライアントがタスクの受け入れを送信する前に、このプロパティをタスクの割り当て先の名前に設定します。</span><span class="sxs-lookup"><span data-stu-id="c44ee-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="c44ee-119">クライアントがタスク拒否を送信する前に、このプロパティをタスク割り当て者の名前に設定します。</span><span class="sxs-lookup"><span data-stu-id="c44ee-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c44ee-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c44ee-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c44ee-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c44ee-121">Protocol specifications</span></span>

<span data-ttu-id="c44ee-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c44ee-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c44ee-123">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="c44ee-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c44ee-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c44ee-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c44ee-125">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="c44ee-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c44ee-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c44ee-126">Header files</span></span>

<span data-ttu-id="c44ee-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c44ee-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c44ee-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c44ee-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c44ee-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c44ee-129">See also</span></span>



[<span data-ttu-id="c44ee-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c44ee-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c44ee-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c44ee-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c44ee-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c44ee-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c44ee-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c44ee-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

