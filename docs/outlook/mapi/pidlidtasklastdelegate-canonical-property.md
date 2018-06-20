---
title: PidLidTaskLastDelegate の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8e1a343486e78daae45ca7315ba4d29d44b688bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802214"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="6a26d-103">PidLidTaskLastDelegate の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6a26d-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="6a26d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6a26d-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="6a26d-105">最も最近割り当てられているか、タスクを割り当てられたユーザーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="6a26d-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a26d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="6a26d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6a26d-107">dispidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="6a26d-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="6a26d-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6a26d-108">Property set:</span></span>  <br/> |<span data-ttu-id="6a26d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="6a26d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="6a26d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6a26d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6a26d-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="6a26d-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="6a26d-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="6a26d-112">Data type:</span></span>  <br/> |<span data-ttu-id="6a26d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6a26d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6a26d-114">領域:</span><span class="sxs-lookup"><span data-stu-id="6a26d-114">Area:</span></span>  <br/> |<span data-ttu-id="6a26d-115">タスク</span><span class="sxs-lookup"><span data-stu-id="6a26d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a26d-116">備考</span><span class="sxs-lookup"><span data-stu-id="6a26d-116">Remarks</span></span>

<span data-ttu-id="6a26d-117">仕事の依頼を送信する前に、クライアントは、作業仕事を割り当てた人の名前にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6a26d-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="6a26d-118">タスクの応答を送信する前に、クライアントは、タスク実施者の名前にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6a26d-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6a26d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6a26d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6a26d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6a26d-120">Protocol specifications</span></span>

<span data-ttu-id="6a26d-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a26d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a26d-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6a26d-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6a26d-123">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a26d-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a26d-124">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="6a26d-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6a26d-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6a26d-125">Header files</span></span>

<span data-ttu-id="6a26d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6a26d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a26d-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6a26d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a26d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="6a26d-128">See also</span></span>



[<span data-ttu-id="6a26d-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6a26d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a26d-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6a26d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a26d-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="6a26d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a26d-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="6a26d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

