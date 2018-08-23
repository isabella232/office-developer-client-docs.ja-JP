---
title: PidLidTaskMultipleRecipients 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMultipleRecipients
api_type:
- COM
ms.assetid: 28ba9997-72dd-465f-94a7-35a317a361ef
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1e1cba3d927072cb03dbd34eee518c9b0a9e0383
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802224"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="76c9e-103">PidLidTaskMultipleRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="76c9e-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="76c9e-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76c9e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76c9e-105">タスクの受信者についての最適化のヒントを提供します。</span><span class="sxs-lookup"><span data-stu-id="76c9e-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76c9e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="76c9e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76c9e-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="76c9e-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="76c9e-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="76c9e-108">Property set:</span></span>  <br/> |<span data-ttu-id="76c9e-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="76c9e-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="76c9e-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="76c9e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="76c9e-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="76c9e-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="76c9e-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="76c9e-112">Data type:</span></span>  <br/> |<span data-ttu-id="76c9e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="76c9e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="76c9e-114">領域:</span><span class="sxs-lookup"><span data-stu-id="76c9e-114">Area:</span></span>  <br/> |<span data-ttu-id="76c9e-115">タスク</span><span class="sxs-lookup"><span data-stu-id="76c9e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76c9e-116">注釈</span><span class="sxs-lookup"><span data-stu-id="76c9e-116">Remarks</span></span>

<span data-ttu-id="76c9e-117">かどうかこのオプションを設定すると、この必要がありますプロパティに次の値の 0 個以上のビットごとの**OR**演算されます。</span><span class="sxs-lookup"><span data-stu-id="76c9e-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="76c9e-118">**名前**</span><span class="sxs-lookup"><span data-stu-id="76c9e-118">**Name**</span></span>|<span data-ttu-id="76c9e-119">**値**</span><span class="sxs-lookup"><span data-stu-id="76c9e-119">**Value**</span></span>|<span data-ttu-id="76c9e-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="76c9e-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="76c9e-121">Sent</span><span class="sxs-lookup"><span data-stu-id="76c9e-121">Sent</span></span>  <br/> |<span data-ttu-id="76c9e-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="76c9e-122">0x00000001</span></span>  <br/> |<span data-ttu-id="76c9e-123">タスクには、複数の主な受信者があります。</span><span class="sxs-lookup"><span data-stu-id="76c9e-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="76c9e-124">Received</span><span class="sxs-lookup"><span data-stu-id="76c9e-124">Received</span></span>  <br/> |<span data-ttu-id="76c9e-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="76c9e-125">0x00000002</span></span>  <br/> |<span data-ttu-id="76c9e-126">送信済みアイテムのヒントは存在しませんでした、ですが、タスクが複数の主な受信者を持っているクライアントを検出しました。</span><span class="sxs-lookup"><span data-stu-id="76c9e-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="76c9e-127">Reserved</span><span class="sxs-lookup"><span data-stu-id="76c9e-127">Reserved</span></span>  <br/> |<span data-ttu-id="76c9e-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="76c9e-128">0x00000004</span></span>  <br/> |<span data-ttu-id="76c9e-129">この値は予約されています。</span><span class="sxs-lookup"><span data-stu-id="76c9e-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="76c9e-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="76c9e-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="76c9e-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="76c9e-131">Protocol specifications</span></span>

<span data-ttu-id="76c9e-132">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76c9e-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76c9e-133">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="76c9e-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="76c9e-134">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76c9e-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76c9e-135">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="76c9e-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="76c9e-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="76c9e-136">Header files</span></span>

<span data-ttu-id="76c9e-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76c9e-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="76c9e-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="76c9e-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76c9e-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="76c9e-139">See also</span></span>



[<span data-ttu-id="76c9e-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="76c9e-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76c9e-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="76c9e-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76c9e-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="76c9e-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76c9e-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="76c9e-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

