---
title: PidLidTaskFCreator 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFCreator
api_type:
- COM
ms.assetid: bb88750b-4773-4241-aa38-462a2634dbcb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dfb49fafcc2dc368e84786b526869e0447ccaf8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303081"
---
# <a name="pidlidtaskfcreator-canonical-property"></a><span data-ttu-id="fa5cc-103">PidLidTaskFCreator 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fa5cc-103">PidLidTaskFCreator Canonical Property</span></span>

  
  
<span data-ttu-id="fa5cc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa5cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa5cc-105">タスク要求を処理するのではなく、現在のユーザーまたはユーザー エージェントによって作成されたタスクを示します。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-105">Indicates the task was originally created by the current user or user agent instead of by processing a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa5cc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fa5cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fa5cc-107">dispidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="fa5cc-107">dispidTaskFCreator</span></span>  <br/> |
|<span data-ttu-id="fa5cc-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="fa5cc-108">Property set:</span></span>  <br/> |<span data-ttu-id="fa5cc-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="fa5cc-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="fa5cc-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fa5cc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fa5cc-111">0x0000811E</span><span class="sxs-lookup"><span data-stu-id="fa5cc-111">0x0000811E</span></span>  <br/> |
|<span data-ttu-id="fa5cc-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fa5cc-112">Data type:</span></span>  <br/> |<span data-ttu-id="fa5cc-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fa5cc-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fa5cc-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="fa5cc-114">Area:</span></span>  <br/> |<span data-ttu-id="fa5cc-115">タスク</span><span class="sxs-lookup"><span data-stu-id="fa5cc-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa5cc-116">注釈</span><span class="sxs-lookup"><span data-stu-id="fa5cc-116">Remarks</span></span>

<span data-ttu-id="fa5cc-117">クライアントは、ユーザーがタスクを作成するときにこのプロパティを TRUE に設定し、タスクが別のユーザーによって割り当てられている場合は FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-117">The client sets this property to TRUE when the user creates the task and to FALSE when the task is assigned by another user.</span></span> <span data-ttu-id="fa5cc-118">このプロパティを設定しない場合は、TRUE の値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-118">If this property is left unset, a value of TRUE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fa5cc-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fa5cc-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fa5cc-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fa5cc-120">Protocol specifications</span></span>

<span data-ttu-id="fa5cc-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa5cc-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa5cc-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fa5cc-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa5cc-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa5cc-124">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fa5cc-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fa5cc-125">Header files</span></span>

<span data-ttu-id="fa5cc-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa5cc-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fa5cc-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fa5cc-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa5cc-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa5cc-128">See also</span></span>



[<span data-ttu-id="fa5cc-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fa5cc-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fa5cc-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fa5cc-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fa5cc-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fa5cc-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fa5cc-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fa5cc-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

