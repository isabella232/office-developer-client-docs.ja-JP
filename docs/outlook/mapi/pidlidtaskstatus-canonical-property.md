---
title: PidLidTaskStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStatus
api_type:
- COM
ms.assetid: 809776b7-ff00-4a52-84b9-8b5fb5f5c3e3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a89cf096e3775b57035be60cab01e3d687770cf8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582575"
---
# <a name="pidlidtaskstatus-canonical-property"></a><span data-ttu-id="191c8-103">PidLidTaskStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="191c8-103">PidLidTaskStatus Canonical Property</span></span>

  
  
<span data-ttu-id="191c8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="191c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="191c8-105">タスクのユーザーの進行状況のステータスを指定します。</span><span class="sxs-lookup"><span data-stu-id="191c8-105">Specifies the status of the user's progress on the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="191c8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="191c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="191c8-107">dispidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="191c8-107">dispidTaskStatus</span></span>  <br/> |
|<span data-ttu-id="191c8-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="191c8-108">Property set:</span></span>  <br/> |<span data-ttu-id="191c8-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="191c8-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="191c8-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="191c8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="191c8-111">0x00008101</span><span class="sxs-lookup"><span data-stu-id="191c8-111">0x00008101</span></span>  <br/> |
|<span data-ttu-id="191c8-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="191c8-112">Data type:</span></span>  <br/> |<span data-ttu-id="191c8-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="191c8-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="191c8-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="191c8-114">Area:</span></span>  <br/> |<span data-ttu-id="191c8-115">タスク</span><span class="sxs-lookup"><span data-stu-id="191c8-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="191c8-116">注釈</span><span class="sxs-lookup"><span data-stu-id="191c8-116">Remarks</span></span>

<span data-ttu-id="191c8-117">このプロパティの値を次のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="191c8-117">The value of this property must be set to one of the following.</span></span>
  
|<span data-ttu-id="191c8-118">**値**</span><span class="sxs-lookup"><span data-stu-id="191c8-118">**Value**</span></span>|<span data-ttu-id="191c8-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="191c8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="191c8-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="191c8-120">0x00000000</span></span>  <br/> |<span data-ttu-id="191c8-121">ユーザーは、タスクの作業を開始されていません。</span><span class="sxs-lookup"><span data-stu-id="191c8-121">The user has not started work on the task.</span></span> <span data-ttu-id="191c8-122">この値が設定されている場合、 **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) は、0.0 をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="191c8-122">If this value is set, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) must be 0.0.</span></span>  <br/> |
|<span data-ttu-id="191c8-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="191c8-123">0x00000001</span></span>  <br/> |<span data-ttu-id="191c8-124">このタスクでのユーザーの作業は進行中です。</span><span class="sxs-lookup"><span data-stu-id="191c8-124">The user's work on this task is in progress.</span></span> <span data-ttu-id="191c8-125">この値が設定されている場合、 **dispidPercentComplete**は 0.0 および 1.0 未満の場合よりも大きくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="191c8-125">If this value is set, **dispidPercentComplete** must be greater than 0.0 and less than 1.0.</span></span>  <br/> |
|<span data-ttu-id="191c8-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="191c8-126">0x00000002</span></span>  <br/> |<span data-ttu-id="191c8-127">このタスクでのユーザーの作業は完了です。</span><span class="sxs-lookup"><span data-stu-id="191c8-127">The user's work on this task is complete.</span></span> <span data-ttu-id="191c8-128">この値が設定されている場合は、 **dispidPercentComplete**は 1.0 である必要があり、 **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) は、現在の日付である必要があります**dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) は TRUE である必要があります。</span><span class="sxs-lookup"><span data-stu-id="191c8-128">If this value is set, **dispidPercentComplete** must be 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) must be the current date, and **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) must be TRUE.</span></span>  <br/> |
|<span data-ttu-id="191c8-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="191c8-129">0x00000003</span></span>  <br/> |<span data-ttu-id="191c8-130">ユーザーは、他のユーザーに待機しています。</span><span class="sxs-lookup"><span data-stu-id="191c8-130">The user is waiting on somebody else.</span></span>  <br/> |
|<span data-ttu-id="191c8-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="191c8-131">0x00000004</span></span>  <br/> |<span data-ttu-id="191c8-132">ユーザーは、タスクの作業を延期しました。</span><span class="sxs-lookup"><span data-stu-id="191c8-132">The user has deferred work on the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="191c8-133">関連リソース</span><span class="sxs-lookup"><span data-stu-id="191c8-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="191c8-134">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="191c8-134">Protocol specifications</span></span>

<span data-ttu-id="191c8-135">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="191c8-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="191c8-136">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="191c8-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="191c8-137">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="191c8-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="191c8-138">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="191c8-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="191c8-139">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="191c8-139">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="191c8-140">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="191c8-140">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="191c8-141">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="191c8-141">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="191c8-142">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="191c8-142">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="191c8-143">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="191c8-143">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="191c8-144">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="191c8-144">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="191c8-145">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="191c8-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="191c8-146">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="191c8-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="191c8-147">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="191c8-147">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="191c8-148">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="191c8-148">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="191c8-149">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="191c8-149">Header files</span></span>

<span data-ttu-id="191c8-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="191c8-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="191c8-151">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="191c8-151">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="191c8-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="191c8-152">See also</span></span>



[<span data-ttu-id="191c8-153">PidLidPercentComplete 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="191c8-153">PidLidPercentComplete Canonical Property</span></span>](pidlidpercentcomplete-canonical-property.md)
  
[<span data-ttu-id="191c8-154">PidLidTaskDateCompleted 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="191c8-154">PidLidTaskDateCompleted Canonical Property</span></span>](pidlidtaskdatecompleted-canonical-property.md)
  
[<span data-ttu-id="191c8-155">PidLidTaskComplete 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="191c8-155">PidLidTaskComplete Canonical Property</span></span>](pidlidtaskcomplete-canonical-property.md)


[<span data-ttu-id="191c8-156">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="191c8-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="191c8-157">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="191c8-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="191c8-158">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="191c8-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="191c8-159">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="191c8-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

