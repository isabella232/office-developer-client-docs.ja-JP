---
title: PidLidTaskDateCompleted 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDateCompleted
api_type:
- COM
ms.assetid: ae384529-55e2-4da1-9a41-acc292591a7c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3096e7ab2133d2984be0534cb091d61d2c7157bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303214"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a><span data-ttu-id="fabc7-103">PidLidTaskDateCompleted 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fabc7-103">PidLidTaskDateCompleted Canonical Property</span></span>

  
  
<span data-ttu-id="fabc7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fabc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fabc7-105">ユーザーがタスクを完了した日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="fabc7-105">Specifies the date when the user completes the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fabc7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fabc7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fabc7-107">dispidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="fabc7-107">dispidTaskDateCompleted</span></span>  <br/> |
|<span data-ttu-id="fabc7-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="fabc7-108">Property set:</span></span>  <br/> |<span data-ttu-id="fabc7-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="fabc7-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="fabc7-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fabc7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fabc7-111">0x0000810f</span><span class="sxs-lookup"><span data-stu-id="fabc7-111">0x0000810F</span></span>  <br/> |
|<span data-ttu-id="fabc7-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fabc7-112">Data type:</span></span>  <br/> |<span data-ttu-id="fabc7-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="fabc7-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="fabc7-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="fabc7-114">Area:</span></span>  <br/> |<span data-ttu-id="fabc7-115">タスク</span><span class="sxs-lookup"><span data-stu-id="fabc7-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fabc7-116">解説</span><span class="sxs-lookup"><span data-stu-id="fabc7-116">Remarks</span></span>

<span data-ttu-id="fabc7-117">設定されている場合、このプロパティには、現地のタイムゾーンでの午前0時の時刻コンポーネントがあり、協定世界時 (UTC) に変換される必要があります。</span><span class="sxs-lookup"><span data-stu-id="fabc7-117">If set, this property must have a time component of midnight in the local time zone, converted to Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fabc7-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fabc7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fabc7-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fabc7-119">Protocol specifications</span></span>

<span data-ttu-id="fabc7-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fabc7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fabc7-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fabc7-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fabc7-122">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fabc7-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fabc7-123">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="fabc7-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="fabc7-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="fabc7-124">Header files</span></span>

<span data-ttu-id="fabc7-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fabc7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fabc7-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fabc7-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fabc7-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="fabc7-127">See also</span></span>



[<span data-ttu-id="fabc7-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fabc7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fabc7-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fabc7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fabc7-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fabc7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fabc7-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fabc7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

