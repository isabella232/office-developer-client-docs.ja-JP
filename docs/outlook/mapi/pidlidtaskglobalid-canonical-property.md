---
title: PidLidTaskGlobalId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskGlobalId
api_type:
- COM
ms.assetid: 369d8c78-3cf6-4a55-ba14-9da0377d6ccf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 33f3b8e7d3d0e0d4461c947aa8e9b3ee66373d2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802203"
---
# <a name="pidlidtaskglobalid-canonical-property"></a><span data-ttu-id="4d6b0-103">PidLidTaskGlobalId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4d6b0-103">PidLidTaskGlobalId Canonical Property</span></span>

  
  
<span data-ttu-id="4d6b0-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4d6b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4d6b0-105">タスクの応答またはタスクの更新の受信時に、GUID を使用して、既存のタスクを検索します。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-105">Locates an existing task, by using a GUID, upon receipt of a task response or task update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d6b0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4d6b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d6b0-107">dispidTaskGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="4d6b0-107">dispidTaskGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="4d6b0-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-108">Property set:</span></span>  <br/> |<span data-ttu-id="4d6b0-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4d6b0-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4d6b0-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4d6b0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4d6b0-111">0x00008519</span><span class="sxs-lookup"><span data-stu-id="4d6b0-111">0x00008519</span></span>  <br/> |
|<span data-ttu-id="4d6b0-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4d6b0-112">Data type:</span></span>  <br/> |<span data-ttu-id="4d6b0-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4d6b0-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4d6b0-114">領域:</span><span class="sxs-lookup"><span data-stu-id="4d6b0-114">Area:</span></span>  <br/> |<span data-ttu-id="4d6b0-115">タスク</span><span class="sxs-lookup"><span data-stu-id="4d6b0-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d6b0-116">注釈</span><span class="sxs-lookup"><span data-stu-id="4d6b0-116">Remarks</span></span>

<span data-ttu-id="4d6b0-117">このプロパティは、割り当てられていないタスクの設定を解除に残されています。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-117">This property is left unset for unassigned tasks.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4d6b0-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4d6b0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4d6b0-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4d6b0-119">Protocol specifications</span></span>

<span data-ttu-id="4d6b0-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d6b0-120">[[MS-OXPROPS] ](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d6b0-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4d6b0-122">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d6b0-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d6b0-123">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4d6b0-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4d6b0-124">Header files</span></span>

<span data-ttu-id="4d6b0-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d6b0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d6b0-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d6b0-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="4d6b0-127">See also</span></span>



[<span data-ttu-id="4d6b0-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4d6b0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d6b0-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4d6b0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d6b0-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4d6b0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d6b0-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4d6b0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

