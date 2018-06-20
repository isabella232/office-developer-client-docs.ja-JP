---
title: PidLidTaskOwnership の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOwnership
api_type:
- COM
ms.assetid: 805dcb6c-f405-4c4d-8bca-af4bd9cd44fa
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 17f3ac0c5cd6005329212d0dcb458b37bb75f41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802242"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="41296-103">PidLidTaskOwnership の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="41296-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="41296-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41296-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="41296-105">タスクに対する現在のユーザーの役割を示します。</span><span class="sxs-lookup"><span data-stu-id="41296-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="41296-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="41296-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41296-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="41296-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="41296-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="41296-108">Property set:</span></span>  <br/> |<span data-ttu-id="41296-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="41296-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="41296-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="41296-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="41296-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="41296-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="41296-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="41296-112">Data type:</span></span>  <br/> |<span data-ttu-id="41296-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="41296-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="41296-114">領域:</span><span class="sxs-lookup"><span data-stu-id="41296-114">Area:</span></span>  <br/> |<span data-ttu-id="41296-115">タスク</span><span class="sxs-lookup"><span data-stu-id="41296-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41296-116">備考</span><span class="sxs-lookup"><span data-stu-id="41296-116">Remarks</span></span>

<span data-ttu-id="41296-117">このプロパティは、次の値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="41296-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="41296-118">**値**</span><span class="sxs-lookup"><span data-stu-id="41296-118">**Value**</span></span>|<span data-ttu-id="41296-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="41296-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41296-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41296-120">0x00000000</span></span>  <br/> |<span data-ttu-id="41296-121">タスクが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="41296-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="41296-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="41296-122">0x00000001</span></span>  <br/> |<span data-ttu-id="41296-123">タスクは、タスクの作業仕事を割り当てた人のコピーです。</span><span class="sxs-lookup"><span data-stu-id="41296-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="41296-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="41296-124">0x00000002</span></span>  <br/> |<span data-ttu-id="41296-125">タスクは、タスクのタスク実施者のコピーです。</span><span class="sxs-lookup"><span data-stu-id="41296-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="41296-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="41296-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="41296-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="41296-127">Protocol specifications</span></span>

<span data-ttu-id="41296-128">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41296-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41296-129">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="41296-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="41296-130">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41296-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41296-131">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="41296-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="41296-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="41296-132">Header files</span></span>

<span data-ttu-id="41296-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41296-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="41296-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="41296-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41296-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="41296-135">See also</span></span>



[<span data-ttu-id="41296-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="41296-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41296-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="41296-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41296-138">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="41296-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41296-139">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="41296-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

