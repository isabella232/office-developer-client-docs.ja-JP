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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390934"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="320ef-103">PidLidTaskLastUser 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="320ef-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="320ef-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="320ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="320ef-105">最新のユーザーがタスクの所有者の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="320ef-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="320ef-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="320ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="320ef-107">dispidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="320ef-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="320ef-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="320ef-108">Property set:</span></span>  <br/> |<span data-ttu-id="320ef-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="320ef-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="320ef-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="320ef-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="320ef-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="320ef-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="320ef-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="320ef-112">Data type:</span></span>  <br/> |<span data-ttu-id="320ef-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="320ef-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="320ef-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="320ef-114">Area:</span></span>  <br/> |<span data-ttu-id="320ef-115">タスク</span><span class="sxs-lookup"><span data-stu-id="320ef-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="320ef-116">備考</span><span class="sxs-lookup"><span data-stu-id="320ef-116">Remarks</span></span>

<span data-ttu-id="320ef-117">クライアントでは、仕事の依頼を送信する前に、仕事のタスクを割り当てた人の名前にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="320ef-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="320ef-118">クライアントでは、仕事の承諾を送信する前に、タスク実施者の名前にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="320ef-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="320ef-119">クライアントは、タスクの辞退を送信する前に、仕事のタスクを割り当てた人の名前にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="320ef-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="320ef-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="320ef-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="320ef-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="320ef-121">Protocol specifications</span></span>

<span data-ttu-id="320ef-122">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="320ef-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="320ef-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="320ef-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="320ef-124">[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="320ef-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="320ef-125">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="320ef-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="320ef-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="320ef-126">Header files</span></span>

<span data-ttu-id="320ef-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="320ef-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="320ef-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="320ef-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="320ef-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="320ef-129">See also</span></span>



[<span data-ttu-id="320ef-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="320ef-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="320ef-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="320ef-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="320ef-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="320ef-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="320ef-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="320ef-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

