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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5700ab6baaab2a5e73448582a855e6f243d5361d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303046"
---
# <a name="pidlidtaskestimatedeffort-canonical-property"></a><span data-ttu-id="28daf-103">PidLidTaskEstimatedEffort 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="28daf-103">PidLidTaskEstimatedEffort Canonical Property</span></span>

  
  
<span data-ttu-id="28daf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28daf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28daf-105">ユーザーがタスクを実行する時間を分で示します。</span><span class="sxs-lookup"><span data-stu-id="28daf-105">Indicates the amount of time, in minutes, that the user expects to perform a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="28daf-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="28daf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="28daf-107">dispidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="28daf-107">dispidTaskEstimatedEffort</span></span>  <br/> |
|<span data-ttu-id="28daf-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="28daf-108">Property set:</span></span>  <br/> |<span data-ttu-id="28daf-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="28daf-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="28daf-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="28daf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="28daf-111">0x00008111</span><span class="sxs-lookup"><span data-stu-id="28daf-111">0x00008111</span></span>  <br/> |
|<span data-ttu-id="28daf-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="28daf-112">Data type:</span></span>  <br/> |<span data-ttu-id="28daf-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="28daf-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="28daf-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="28daf-114">Area:</span></span>  <br/> |<span data-ttu-id="28daf-115">タスク</span><span class="sxs-lookup"><span data-stu-id="28daf-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28daf-116">注釈</span><span class="sxs-lookup"><span data-stu-id="28daf-116">Remarks</span></span>

<span data-ttu-id="28daf-117">値は 0 以上 0x5AE980DF (1,525,252,319) 以下である必要があります。480 分は 1 日に等しく、2400 分は 1 週間 (1 日に 8 時間、1 週間で 5 日間)。</span><span class="sxs-lookup"><span data-stu-id="28daf-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="28daf-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="28daf-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="28daf-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="28daf-119">Protocol specifications</span></span>

<span data-ttu-id="28daf-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28daf-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28daf-121">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="28daf-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="28daf-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28daf-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28daf-123">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="28daf-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="28daf-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="28daf-124">Header files</span></span>

<span data-ttu-id="28daf-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28daf-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="28daf-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="28daf-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28daf-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="28daf-127">See also</span></span>



[<span data-ttu-id="28daf-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="28daf-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="28daf-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="28daf-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="28daf-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="28daf-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="28daf-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="28daf-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

