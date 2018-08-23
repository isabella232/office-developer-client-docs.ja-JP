---
title: PidLidTaskDeadOccurrence 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDeadOccurrence
api_type:
- COM
ms.assetid: e78287ff-f8cc-45ea-8da8-e7a7359e651c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5fca47055d0c88293156483a53118667c1c72276
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574099"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a><span data-ttu-id="ac282-103">PidLidTaskDeadOccurrence 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac282-103">PidLidTaskDeadOccurrence Canonical Property</span></span>

  
  
<span data-ttu-id="ac282-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac282-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac282-105">新しい文字列を生成する必要があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ac282-105">Indicates whether new occurrences must be generated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac282-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ac282-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac282-107">dispidTaskDeadOccur</span><span class="sxs-lookup"><span data-stu-id="ac282-107">dispidTaskDeadOccur</span></span>  <br/> |
|<span data-ttu-id="ac282-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="ac282-108">Property set:</span></span>  <br/> |<span data-ttu-id="ac282-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="ac282-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="ac282-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ac282-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ac282-111">0x00008109</span><span class="sxs-lookup"><span data-stu-id="ac282-111">0x00008109</span></span>  <br/> |
|<span data-ttu-id="ac282-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ac282-112">Data type:</span></span>  <br/> |<span data-ttu-id="ac282-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ac282-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ac282-114">領域:</span><span class="sxs-lookup"><span data-stu-id="ac282-114">Area:</span></span>  <br/> |<span data-ttu-id="ac282-115">タスク</span><span class="sxs-lookup"><span data-stu-id="ac282-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac282-116">注釈</span><span class="sxs-lookup"><span data-stu-id="ac282-116">Remarks</span></span>

<span data-ttu-id="ac282-117">定期的なパターンになって実際に過去の最後のインスタンスは、または、指定されたインスタンス数が生成されたとき。</span><span class="sxs-lookup"><span data-stu-id="ac282-117">A recurrence pattern is no longer in effect when its final instance is in the past or its specified number of instances has been generated.</span></span> <span data-ttu-id="ac282-118">クライアント プロパティを設定この新しいタスクを FALSE または true を指定して定期的な仕事の最後のインスタンスを生成するとき。</span><span class="sxs-lookup"><span data-stu-id="ac282-118">The client sets this property to FALSE for a new task or to TRUE when it generates the last instance of a recurring task.</span></span> <span data-ttu-id="ac282-119">新しいインスタンスを生成するタスクをコピーすると、完了したインスタンスでは、コピーで、このプロパティが TRUE に設定が。</span><span class="sxs-lookup"><span data-stu-id="ac282-119">When you copy a task to generate a new instance, this property is set to TRUE on the copy, which is the completed instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ac282-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ac282-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac282-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ac282-121">Protocol specifications</span></span>

<span data-ttu-id="ac282-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac282-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac282-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ac282-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ac282-124">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac282-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac282-125">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="ac282-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="ac282-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ac282-126">Header files</span></span>

<span data-ttu-id="ac282-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac282-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac282-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ac282-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac282-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac282-129">See also</span></span>



[<span data-ttu-id="ac282-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac282-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac282-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac282-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac282-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ac282-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac282-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ac282-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

