---
title: PidLidTaskLastUser の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6dc2bcf2003ee16fa4a6c66689b6af79653e2d04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802219"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="e9ba7-103">PidLidTaskLastUser の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e9ba7-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="e9ba7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9ba7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9ba7-105">最新のユーザーがタスクの所有者の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e9ba7-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9ba7-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="e9ba7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9ba7-107">dispidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="e9ba7-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="e9ba7-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e9ba7-108">Property set:</span></span>  <br/> |<span data-ttu-id="e9ba7-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e9ba7-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e9ba7-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e9ba7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e9ba7-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="e9ba7-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="e9ba7-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="e9ba7-112">Data type:</span></span>  <br/> |<span data-ttu-id="e9ba7-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e9ba7-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e9ba7-114">領域:</span><span class="sxs-lookup"><span data-stu-id="e9ba7-114">Area:</span></span>  <br/> |<span data-ttu-id="e9ba7-115">タスク</span><span class="sxs-lookup"><span data-stu-id="e9ba7-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9ba7-116">備考</span><span class="sxs-lookup"><span data-stu-id="e9ba7-116">Remarks</span></span>

<span data-ttu-id="e9ba7-117">クライアントでは、仕事の依頼を送信する前に、仕事のタスクを割り当てた人の名前にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e9ba7-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="e9ba7-118">クライアントでは、仕事の承諾を送信する前に、タスク実施者の名前にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e9ba7-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="e9ba7-119">クライアントは、タスクの辞退を送信する前に、仕事のタスクを割り当てた人の名前にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e9ba7-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e9ba7-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e9ba7-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9ba7-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e9ba7-121">Protocol specifications</span></span>

<span data-ttu-id="e9ba7-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9ba7-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9ba7-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e9ba7-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9ba7-124">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9ba7-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9ba7-125">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="e9ba7-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9ba7-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e9ba7-126">Header files</span></span>

<span data-ttu-id="e9ba7-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9ba7-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9ba7-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e9ba7-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9ba7-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9ba7-129">See also</span></span>



[<span data-ttu-id="e9ba7-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9ba7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9ba7-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9ba7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9ba7-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="e9ba7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9ba7-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="e9ba7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

