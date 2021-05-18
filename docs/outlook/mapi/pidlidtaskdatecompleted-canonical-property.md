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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3096e7ab2133d2984be0534cb091d61d2c7157bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303214"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a><span data-ttu-id="bb663-103">PidLidTaskDateCompleted 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb663-103">PidLidTaskDateCompleted Canonical Property</span></span>

  
  
<span data-ttu-id="bb663-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb663-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb663-105">ユーザーがタスクを完了する日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb663-105">Specifies the date when the user completes the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb663-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bb663-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb663-107">dispidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="bb663-107">dispidTaskDateCompleted</span></span>  <br/> |
|<span data-ttu-id="bb663-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="bb663-108">Property set:</span></span>  <br/> |<span data-ttu-id="bb663-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="bb663-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="bb663-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bb663-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bb663-111">0x0000810F</span><span class="sxs-lookup"><span data-stu-id="bb663-111">0x0000810F</span></span>  <br/> |
|<span data-ttu-id="bb663-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bb663-112">Data type:</span></span>  <br/> |<span data-ttu-id="bb663-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="bb663-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="bb663-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="bb663-114">Area:</span></span>  <br/> |<span data-ttu-id="bb663-115">タスク</span><span class="sxs-lookup"><span data-stu-id="bb663-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb663-116">注釈</span><span class="sxs-lookup"><span data-stu-id="bb663-116">Remarks</span></span>

<span data-ttu-id="bb663-117">このプロパティを設定する場合は、ローカル タイム ゾーンの時刻コンポーネントが午前 0 時で、協定世界時 (UTC) に変換されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb663-117">If set, this property must have a time component of midnight in the local time zone, converted to Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bb663-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bb663-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb663-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bb663-119">Protocol specifications</span></span>

<span data-ttu-id="bb663-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb663-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb663-121">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="bb663-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb663-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb663-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb663-123">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="bb663-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="bb663-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bb663-124">Header files</span></span>

<span data-ttu-id="bb663-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb663-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb663-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bb663-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb663-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb663-127">See also</span></span>



[<span data-ttu-id="bb663-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bb663-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb663-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb663-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb663-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bb663-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb663-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bb663-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

