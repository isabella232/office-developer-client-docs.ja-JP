---
title: PidLidTaskEstimatedEffort 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskEstimatedEffort
api_type:
- COM
ms.assetid: c84167d8-f726-45c6-9b21-bcde64473148
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 987188db4a3aceb4b065f59cdf449f943f68e70d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565320"
---
# <a name="pidlidtaskestimatedeffort-canonical-property"></a><span data-ttu-id="4a8c3-103">PidLidTaskEstimatedEffort 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a8c3-103">PidLidTaskEstimatedEffort Canonical Property</span></span>

  
  
<span data-ttu-id="4a8c3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a8c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a8c3-105">時間 (分)、ユーザーがタスクを実行する要求の量を示します。</span><span class="sxs-lookup"><span data-stu-id="4a8c3-105">Indicates the amount of time, in minutes, that the user expects to perform a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a8c3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4a8c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a8c3-107">dispidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="4a8c3-107">dispidTaskEstimatedEffort</span></span>  <br/> |
|<span data-ttu-id="4a8c3-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4a8c3-108">Property set:</span></span>  <br/> |<span data-ttu-id="4a8c3-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="4a8c3-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="4a8c3-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4a8c3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4a8c3-111">0x00008111</span><span class="sxs-lookup"><span data-stu-id="4a8c3-111">0x00008111</span></span>  <br/> |
|<span data-ttu-id="4a8c3-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4a8c3-112">Data type:</span></span>  <br/> |<span data-ttu-id="4a8c3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4a8c3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4a8c3-114">領域:</span><span class="sxs-lookup"><span data-stu-id="4a8c3-114">Area:</span></span>  <br/> |<span data-ttu-id="4a8c3-115">タスク</span><span class="sxs-lookup"><span data-stu-id="4a8c3-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a8c3-116">注釈</span><span class="sxs-lookup"><span data-stu-id="4a8c3-116">Remarks</span></span>

<span data-ttu-id="4a8c3-117">値は、0 以上で 0x5AE980DF (1,525,252,319) より小さい、480 分と等しい 1 日 2400 分と等しい 1 週間 (1 日の作業で、稼働日の 5 日間は 8 時間) をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a8c3-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4a8c3-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4a8c3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a8c3-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4a8c3-119">Protocol specifications</span></span>

<span data-ttu-id="4a8c3-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a8c3-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a8c3-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4a8c3-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a8c3-122">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a8c3-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a8c3-123">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="4a8c3-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="4a8c3-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4a8c3-124">Header files</span></span>

<span data-ttu-id="4a8c3-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a8c3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a8c3-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4a8c3-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a8c3-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="4a8c3-127">See also</span></span>



[<span data-ttu-id="4a8c3-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a8c3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a8c3-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a8c3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a8c3-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4a8c3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a8c3-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4a8c3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

