---
title: PidLidTaskOrdinal 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a64008da93584529916a9303176bba0aa08d3fac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357961"
---
# <a name="pidlidtaskordinal-canonical-property"></a><span data-ttu-id="e6be6-103">PidLidTaskOrdinal 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e6be6-103">PidLidTaskOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="e6be6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6be6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6be6-105">カスタムの並べ替えタスクを支援します。</span><span class="sxs-lookup"><span data-stu-id="e6be6-105">Provides an aid to custom sorting tasks.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6be6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e6be6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e6be6-107">dispidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="e6be6-107">dispidTaskOrdinal</span></span>  <br/> |
|<span data-ttu-id="e6be6-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="e6be6-108">Property set:</span></span>  <br/> |<span data-ttu-id="e6be6-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e6be6-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e6be6-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e6be6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e6be6-111">0x00008123</span><span class="sxs-lookup"><span data-stu-id="e6be6-111">0x00008123</span></span>  <br/> |
|<span data-ttu-id="e6be6-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e6be6-112">Data type:</span></span>  <br/> |<span data-ttu-id="e6be6-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e6be6-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e6be6-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="e6be6-114">Area:</span></span>  <br/> |<span data-ttu-id="e6be6-115">タスク</span><span class="sxs-lookup"><span data-stu-id="e6be6-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6be6-116">注釈</span><span class="sxs-lookup"><span data-stu-id="e6be6-116">Remarks</span></span>

<span data-ttu-id="e6be6-117">このプロパティは未設定の場合があります。</span><span class="sxs-lookup"><span data-stu-id="e6be6-117">This property may be left unset.</span></span> <span data-ttu-id="e6be6-118">設定する場合、その値は "0x800186A0" (-2,147,383,648) より大きく、"0x7FFE7960" (2,147,383,648) 未満で、同じフォルダー内のタスク間で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6be6-118">If set, its value must be greater than "0x800186A0" (-2,147,383,648) and less than "0x7FFE7960" (2,147,383,648) and must be unique among tasks in the same folder.</span></span>
  
<span data-ttu-id="e6be6-119">クライアントがフォルダーの **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) プロパティの現在の値の負の値より小さい数値にこのプロパティを設定するたびに、クライアントはフォルダーの **PR_ORDINAL_MOST** も更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6be6-119">Whenever the client sets this property to a number less than the negative of the current value of the **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) property of the folder, the client must also update **PR_ORDINAL_MOST** on the folder.</span></span> 
  
<span data-ttu-id="e6be6-120">フォルダー **PR_ORDINAL_MOST** プロパティを使用すると、同じフォルダー内のタスク間で一意の値を効率的に決定できます。</span><span class="sxs-lookup"><span data-stu-id="e6be6-120">The **PR_ORDINAL_MOST** property of the folder provides an efficient way to determine a unique value among tasks in the same folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e6be6-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e6be6-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e6be6-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e6be6-122">Protocol specifications</span></span>

<span data-ttu-id="e6be6-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6be6-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6be6-124">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="e6be6-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e6be6-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6be6-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6be6-126">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="e6be6-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="e6be6-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e6be6-127">Header files</span></span>

<span data-ttu-id="e6be6-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6be6-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="e6be6-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e6be6-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e6be6-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="e6be6-130">See also</span></span>



[<span data-ttu-id="e6be6-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e6be6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e6be6-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e6be6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e6be6-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e6be6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e6be6-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e6be6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

