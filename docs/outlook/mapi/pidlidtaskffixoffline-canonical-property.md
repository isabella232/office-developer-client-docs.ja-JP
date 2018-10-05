---
title: PidLidTaskFFixOffline 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 226e59ef6aa88bc290cf5aeb4d620979f926e1eb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386265"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="55cde-103">PidLidTaskFFixOffline 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="55cde-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="55cde-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55cde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55cde-105">**DispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) のプロパティの正確性を示します。</span><span class="sxs-lookup"><span data-stu-id="55cde-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55cde-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="55cde-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55cde-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="55cde-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="55cde-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="55cde-108">Property set:</span></span>  <br/> |<span data-ttu-id="55cde-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="55cde-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="55cde-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="55cde-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="55cde-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="55cde-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="55cde-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="55cde-112">Data type:</span></span>  <br/> |<span data-ttu-id="55cde-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="55cde-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="55cde-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="55cde-114">Area:</span></span>  <br/> |<span data-ttu-id="55cde-115">タスク</span><span class="sxs-lookup"><span data-stu-id="55cde-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55cde-116">備考</span><span class="sxs-lookup"><span data-stu-id="55cde-116">Remarks</span></span>

<span data-ttu-id="55cde-117">**DispidTaskFFixOffline**プロパティが FALSE に設定が設定されていない場合、 **dispidTaskOwner**プロパティの値が正しい。</span><span class="sxs-lookup"><span data-stu-id="55cde-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="55cde-118">**DispidTaskFFixOffline**が TRUE に設定されている場合、クライアントは、 **dispidTaskOwner**の正確な値を特定できません。</span><span class="sxs-lookup"><span data-stu-id="55cde-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="55cde-119">その場合は、クライアントでは、「不明」などの汎用の所有者の名前に**dispidTaskOwner**を設定できます。</span><span class="sxs-lookup"><span data-stu-id="55cde-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="55cde-120">ただし、クライアントが真の**dispidTaskFFixOffline**の値を検出すると、正確な所有者名を決定することができます、クライアントは**dispidTaskOwner**を更新する必要があり、 **dispidTaskFFixOffline**が FALSE に設定。</span><span class="sxs-lookup"><span data-stu-id="55cde-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="55cde-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="55cde-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55cde-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="55cde-122">Protocol specifications</span></span>

<span data-ttu-id="55cde-123">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55cde-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55cde-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="55cde-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55cde-125">[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55cde-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55cde-126">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="55cde-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="55cde-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="55cde-127">Header files</span></span>

<span data-ttu-id="55cde-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55cde-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="55cde-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="55cde-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55cde-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="55cde-130">See also</span></span>



[<span data-ttu-id="55cde-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="55cde-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55cde-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="55cde-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55cde-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="55cde-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55cde-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="55cde-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

