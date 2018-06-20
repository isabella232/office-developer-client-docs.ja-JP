---
title: PidLidTaskFRecurring の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFRecurring
api_type:
- COM
ms.assetid: 47c9ccbb-161c-4829-8ffb-201f3b54cd45
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: eb97d278640b4cdd2b14152bf4745f883fe2edba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802204"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a><span data-ttu-id="cdf78-103">PidLidTaskFRecurring の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="cdf78-103">PidLidTaskFRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="cdf78-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cdf78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cdf78-105">タスクが定期的なパターンを含めるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="cdf78-105">Indicates whether the task includes a recurrence pattern.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cdf78-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="cdf78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cdf78-107">dispidTaskFRecur</span><span class="sxs-lookup"><span data-stu-id="cdf78-107">dispidTaskFRecur</span></span>  <br/> |
|<span data-ttu-id="cdf78-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="cdf78-108">Property set:</span></span>  <br/> |<span data-ttu-id="cdf78-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="cdf78-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="cdf78-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="cdf78-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cdf78-111">0x00008126</span><span class="sxs-lookup"><span data-stu-id="cdf78-111">0x00008126</span></span>  <br/> |
|<span data-ttu-id="cdf78-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="cdf78-112">Data type:</span></span>  <br/> |<span data-ttu-id="cdf78-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="cdf78-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="cdf78-114">領域:</span><span class="sxs-lookup"><span data-stu-id="cdf78-114">Area:</span></span>  <br/> |<span data-ttu-id="cdf78-115">タスク</span><span class="sxs-lookup"><span data-stu-id="cdf78-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cdf78-116">備考</span><span class="sxs-lookup"><span data-stu-id="cdf78-116">Remarks</span></span>

<span data-ttu-id="cdf78-117">このプロパティが未設定のままには、FALSE の既定値が使われます。</span><span class="sxs-lookup"><span data-stu-id="cdf78-117">If this property is left unset, a default value of FALSE is assumed.</span></span> <span data-ttu-id="cdf78-118">として**dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) のプロパティを設定する必要があります**dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) は TRUE に設定されている場合は、 [[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)で指定します。</span><span class="sxs-lookup"><span data-stu-id="cdf78-118">If it is set to TRUE, the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) and **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) properties must also be set as specified in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cdf78-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cdf78-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cdf78-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cdf78-120">Protocol specifications</span></span>

<span data-ttu-id="cdf78-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdf78-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdf78-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cdf78-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cdf78-123">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdf78-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdf78-124">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="cdf78-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cdf78-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="cdf78-125">Header files</span></span>

<span data-ttu-id="cdf78-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cdf78-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="cdf78-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cdf78-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cdf78-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="cdf78-128">See also</span></span>



[<span data-ttu-id="cdf78-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cdf78-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cdf78-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cdf78-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cdf78-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="cdf78-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cdf78-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="cdf78-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

