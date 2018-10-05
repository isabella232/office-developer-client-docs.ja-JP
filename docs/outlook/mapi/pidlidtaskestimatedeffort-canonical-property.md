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
ms.openlocfilehash: 5700ab6baaab2a5e73448582a855e6f243d5361d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382800"
---
# <a name="pidlidtaskestimatedeffort-canonical-property"></a><span data-ttu-id="9712f-103">PidLidTaskEstimatedEffort 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9712f-103">PidLidTaskEstimatedEffort Canonical Property</span></span>

  
  
<span data-ttu-id="9712f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9712f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9712f-105">時間 (分)、ユーザーがタスクを実行する要求の量を示します。</span><span class="sxs-lookup"><span data-stu-id="9712f-105">Indicates the amount of time, in minutes, that the user expects to perform a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9712f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9712f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9712f-107">dispidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="9712f-107">dispidTaskEstimatedEffort</span></span>  <br/> |
|<span data-ttu-id="9712f-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="9712f-108">Property set:</span></span>  <br/> |<span data-ttu-id="9712f-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="9712f-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="9712f-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9712f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9712f-111">0x00008111</span><span class="sxs-lookup"><span data-stu-id="9712f-111">0x00008111</span></span>  <br/> |
|<span data-ttu-id="9712f-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9712f-112">Data type:</span></span>  <br/> |<span data-ttu-id="9712f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9712f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9712f-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="9712f-114">Area:</span></span>  <br/> |<span data-ttu-id="9712f-115">タスク</span><span class="sxs-lookup"><span data-stu-id="9712f-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9712f-116">備考</span><span class="sxs-lookup"><span data-stu-id="9712f-116">Remarks</span></span>

<span data-ttu-id="9712f-117">値は、0 以上で 0x5AE980DF (1,525,252,319) より小さい、480 分と等しい 1 日 2400 分と等しい 1 週間 (1 日の作業で、稼働日の 5 日間は 8 時間) をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9712f-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9712f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9712f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9712f-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9712f-119">Protocol specifications</span></span>

<span data-ttu-id="9712f-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9712f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9712f-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9712f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9712f-122">[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9712f-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9712f-123">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="9712f-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="9712f-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9712f-124">Header files</span></span>

<span data-ttu-id="9712f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9712f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9712f-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9712f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9712f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="9712f-127">See also</span></span>



[<span data-ttu-id="9712f-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9712f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9712f-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9712f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9712f-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9712f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9712f-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9712f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

