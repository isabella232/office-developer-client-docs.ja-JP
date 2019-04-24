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
ms.openlocfilehash: 295eb9dcc6da7b0fb6c6fd7ea0b73134ffaadb3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303018"
---
# <a name="pidlidtaskglobalid-canonical-property"></a><span data-ttu-id="6303e-103">PidLidTaskGlobalId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6303e-103">PidLidTaskGlobalId Canonical Property</span></span>

  
  
<span data-ttu-id="6303e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6303e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6303e-105">タスクの応答またはタスクの更新を受け取ったときに、GUID を使用して既存のタスクを検索します。</span><span class="sxs-lookup"><span data-stu-id="6303e-105">Locates an existing task, by using a GUID, upon receipt of a task response or task update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6303e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6303e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6303e-107">dispidtaskglobalobjid</span><span class="sxs-lookup"><span data-stu-id="6303e-107">dispidTaskGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="6303e-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="6303e-108">Property set:</span></span>  <br/> |<span data-ttu-id="6303e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6303e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6303e-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6303e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6303e-111">0x00008519</span><span class="sxs-lookup"><span data-stu-id="6303e-111">0x00008519</span></span>  <br/> |
|<span data-ttu-id="6303e-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6303e-112">Data type:</span></span>  <br/> |<span data-ttu-id="6303e-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6303e-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6303e-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="6303e-114">Area:</span></span>  <br/> |<span data-ttu-id="6303e-115">タスク</span><span class="sxs-lookup"><span data-stu-id="6303e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6303e-116">解説</span><span class="sxs-lookup"><span data-stu-id="6303e-116">Remarks</span></span>

<span data-ttu-id="6303e-117">割り当てられていないタスクの場合、このプロパティは未設定のままになります。</span><span class="sxs-lookup"><span data-stu-id="6303e-117">This property is left unset for unassigned tasks.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6303e-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6303e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6303e-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6303e-119">Protocol specifications</span></span>

<span data-ttu-id="6303e-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6303e-120">[[MS-OXPROPS] ](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6303e-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6303e-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6303e-122">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6303e-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6303e-123">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="6303e-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6303e-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="6303e-124">Header files</span></span>

<span data-ttu-id="6303e-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6303e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6303e-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6303e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6303e-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="6303e-127">See also</span></span>



[<span data-ttu-id="6303e-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6303e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6303e-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6303e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6303e-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6303e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6303e-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6303e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

