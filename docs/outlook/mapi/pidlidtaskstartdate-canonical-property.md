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
ms.openlocfilehash: 486b1f913e7c3c76886232c48fa842e25e1f7905
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802231"
---
# <a name="pidlidtaskstartdate-canonical-property"></a><span data-ttu-id="6958a-103">PidLidTaskStartDate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6958a-103">PidLidTaskStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="6958a-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6958a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6958a-105">ユーザーがタスクを開始するのには必要とする日付です。</span><span class="sxs-lookup"><span data-stu-id="6958a-105">The date when the user expects to begin the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6958a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6958a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6958a-107">dispidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="6958a-107">dispidTaskStartDate</span></span>  <br/> |
|<span data-ttu-id="6958a-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6958a-108">Property set:</span></span>  <br/> |<span data-ttu-id="6958a-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="6958a-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="6958a-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6958a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6958a-111">0x00008104</span><span class="sxs-lookup"><span data-stu-id="6958a-111">0x00008104</span></span>  <br/> |
|<span data-ttu-id="6958a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6958a-112">Data type:</span></span>  <br/> |<span data-ttu-id="6958a-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="6958a-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="6958a-114">領域:</span><span class="sxs-lookup"><span data-stu-id="6958a-114">Area:</span></span>  <br/> |<span data-ttu-id="6958a-115">タスク</span><span class="sxs-lookup"><span data-stu-id="6958a-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6958a-116">注釈</span><span class="sxs-lookup"><span data-stu-id="6958a-116">Remarks</span></span>

<span data-ttu-id="6958a-117">このプロパティの値が未設定のままである場合、タスクには開始日はありません。</span><span class="sxs-lookup"><span data-stu-id="6958a-117">If this property value is left unset, the task does not have a start date.</span></span> <span data-ttu-id="6958a-118">"0x5AE980E0"(1,525,252,320) の値は、タスクに開始日がないことも意味します。</span><span class="sxs-lookup"><span data-stu-id="6958a-118">A value of "0x5AE980E0" (1,525,252,320) also means that the task does not have a start date.</span></span> <span data-ttu-id="6958a-119">タスクに開始日がある場合は、値が午前 0 時という時刻成分を持つ必要があり、 **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) と**dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) のプロパティを設定もする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6958a-119">If the task has a start date, the value must have a time component of midnight, and the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) and **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) properties must also be set.</span></span>
  
<span data-ttu-id="6958a-120">情報フラグを設定するプロトコルの仕様でこのプロパティを共有し、Task-Related オブジェクトのプロトコル仕様は、 [[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)にあります。</span><span class="sxs-lookup"><span data-stu-id="6958a-120">This property is shared by the Informational Flagging Protocol Specification and Task-Related Object Protocol Specification located in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6958a-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6958a-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6958a-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6958a-122">Protocol specifications</span></span>

<span data-ttu-id="6958a-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6958a-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6958a-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6958a-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6958a-125">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6958a-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6958a-126">連絡先と個人用配布リストで許可されている操作のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="6958a-126">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6958a-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6958a-127">Header files</span></span>

<span data-ttu-id="6958a-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6958a-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="6958a-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6958a-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6958a-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="6958a-130">See also</span></span>



[<span data-ttu-id="6958a-131">PidLidTaskDueDate ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="6958a-131">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
  
[<span data-ttu-id="6958a-132">PidLidCommonStart ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="6958a-132">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)


[<span data-ttu-id="6958a-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6958a-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6958a-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6958a-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6958a-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6958a-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6958a-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6958a-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

