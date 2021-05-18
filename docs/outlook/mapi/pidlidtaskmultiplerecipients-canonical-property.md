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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3b260917e107086dee6176f73b6c82c3a1825327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360068"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="c9f8a-103">PidLidTaskMultipleRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c9f8a-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="c9f8a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9f8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9f8a-105">タスクの受信者に関する最適化ヒントを提供します。</span><span class="sxs-lookup"><span data-stu-id="c9f8a-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9f8a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c9f8a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9f8a-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="c9f8a-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="c9f8a-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="c9f8a-108">Property set:</span></span>  <br/> |<span data-ttu-id="c9f8a-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="c9f8a-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="c9f8a-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c9f8a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c9f8a-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="c9f8a-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="c9f8a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c9f8a-112">Data type:</span></span>  <br/> |<span data-ttu-id="c9f8a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c9f8a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c9f8a-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="c9f8a-114">Area:</span></span>  <br/> |<span data-ttu-id="c9f8a-115">タスク</span><span class="sxs-lookup"><span data-stu-id="c9f8a-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9f8a-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c9f8a-116">Remarks</span></span>

<span data-ttu-id="c9f8a-117">設定する場合、このプロパティは、次の値の 0 以上のビット **演算 OR** 演算に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9f8a-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="c9f8a-118">**名前**</span><span class="sxs-lookup"><span data-stu-id="c9f8a-118">**Name**</span></span>|<span data-ttu-id="c9f8a-119">**値**</span><span class="sxs-lookup"><span data-stu-id="c9f8a-119">**Value**</span></span>|<span data-ttu-id="c9f8a-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="c9f8a-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9f8a-121">送信日時</span><span class="sxs-lookup"><span data-stu-id="c9f8a-121">Sent</span></span>  <br/> |<span data-ttu-id="c9f8a-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c9f8a-122">0x00000001</span></span>  <br/> |<span data-ttu-id="c9f8a-123">タスクには複数のプライマリ受信者があります。</span><span class="sxs-lookup"><span data-stu-id="c9f8a-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="c9f8a-124">受信済み</span><span class="sxs-lookup"><span data-stu-id="c9f8a-124">Received</span></span>  <br/> |<span data-ttu-id="c9f8a-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c9f8a-125">0x00000002</span></span>  <br/> |<span data-ttu-id="c9f8a-126">送信されたヒントは存在しないが、クライアントはタスクに複数のプライマリ受信者が存在しているのを検出しました。</span><span class="sxs-lookup"><span data-stu-id="c9f8a-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="c9f8a-127">Reserved</span><span class="sxs-lookup"><span data-stu-id="c9f8a-127">Reserved</span></span>  <br/> |<span data-ttu-id="c9f8a-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c9f8a-128">0x00000004</span></span>  <br/> |<span data-ttu-id="c9f8a-129">この値は予約済みです。</span><span class="sxs-lookup"><span data-stu-id="c9f8a-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c9f8a-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c9f8a-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c9f8a-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c9f8a-131">Protocol specifications</span></span>

<span data-ttu-id="c9f8a-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9f8a-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9f8a-133">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="c9f8a-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c9f8a-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9f8a-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9f8a-135">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="c9f8a-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c9f8a-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c9f8a-136">Header files</span></span>

<span data-ttu-id="c9f8a-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9f8a-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9f8a-138">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c9f8a-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9f8a-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="c9f8a-139">See also</span></span>



[<span data-ttu-id="c9f8a-140">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c9f8a-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9f8a-141">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c9f8a-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9f8a-142">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c9f8a-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9f8a-143">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c9f8a-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

