---
title: PidLidTaskStartDate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStartDate
api_type:
- COM
ms.assetid: fe87eb3d-21d1-45bb-b848-e141ce1be6a0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3bc475292e47a9ad8dd9565e17640ef95e7b3c76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316682"
---
# <a name="pidlidtaskstartdate-canonical-property"></a><span data-ttu-id="99e46-103">PidLidTaskStartDate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="99e46-103">PidLidTaskStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="99e46-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99e46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99e46-105">ユーザーがタスクを開始することを期待する日付。</span><span class="sxs-lookup"><span data-stu-id="99e46-105">The date when the user expects to begin the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="99e46-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="99e46-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="99e46-107">dispidtaskstartdate</span><span class="sxs-lookup"><span data-stu-id="99e46-107">dispidTaskStartDate</span></span>  <br/> |
|<span data-ttu-id="99e46-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="99e46-108">Property set:</span></span>  <br/> |<span data-ttu-id="99e46-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="99e46-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="99e46-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="99e46-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="99e46-111">0x00008104</span><span class="sxs-lookup"><span data-stu-id="99e46-111">0x00008104</span></span>  <br/> |
|<span data-ttu-id="99e46-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="99e46-112">Data type:</span></span>  <br/> |<span data-ttu-id="99e46-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="99e46-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="99e46-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="99e46-114">Area:</span></span>  <br/> |<span data-ttu-id="99e46-115">タスク</span><span class="sxs-lookup"><span data-stu-id="99e46-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99e46-116">解説</span><span class="sxs-lookup"><span data-stu-id="99e46-116">Remarks</span></span>

<span data-ttu-id="99e46-117">このプロパティの値が設定されていない場合は、タスクに開始日がありません。</span><span class="sxs-lookup"><span data-stu-id="99e46-117">If this property value is left unset, the task does not have a start date.</span></span> <span data-ttu-id="99e46-118">値 "0x5AE980E0" (1525252320) は、タスクに開始日が設定されていないことも意味します。</span><span class="sxs-lookup"><span data-stu-id="99e46-118">A value of "0x5AE980E0" (1,525,252,320) also means that the task does not have a start date.</span></span> <span data-ttu-id="99e46-119">タスクの開始日が設定されている場合は、その値に午前0時の時間コンポーネントを指定し、 **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) および**dispidcommonstart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) プロパティも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99e46-119">If the task has a start date, the value must have a time component of midnight, and the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) and **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) properties must also be set.</span></span>
  
<span data-ttu-id="99e46-120">このプロパティは、 [[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)にある情報フラグのプロトコル仕様とタスク関連のオブジェクトプロトコル仕様によって共有されます。</span><span class="sxs-lookup"><span data-stu-id="99e46-120">This property is shared by the Informational Flagging Protocol Specification and Task-Related Object Protocol Specification located in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="99e46-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="99e46-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="99e46-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="99e46-122">Protocol specifications</span></span>

<span data-ttu-id="99e46-123">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99e46-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99e46-124">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="99e46-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="99e46-125">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99e46-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99e46-126">連絡先および個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="99e46-126">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="99e46-127">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="99e46-127">Header files</span></span>

<span data-ttu-id="99e46-128">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99e46-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="99e46-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="99e46-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99e46-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="99e46-130">See also</span></span>



[<span data-ttu-id="99e46-131">PidLidTaskDueDate ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="99e46-131">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
  
[<span data-ttu-id="99e46-132">PidLidCommonStart ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="99e46-132">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)


[<span data-ttu-id="99e46-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="99e46-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="99e46-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="99e46-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="99e46-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="99e46-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="99e46-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="99e46-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

