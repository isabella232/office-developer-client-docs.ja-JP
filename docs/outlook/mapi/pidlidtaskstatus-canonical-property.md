---
title: PidLidTaskStatus の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e8ca8d7a82360c1f96448b08c9eda18be502b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802258"
---
# <a name="pidlidtaskstatus-canonical-property"></a><span data-ttu-id="6d22c-103">PidLidTaskStatus の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6d22c-103">PidLidTaskStatus Canonical Property</span></span>

  
  
<span data-ttu-id="6d22c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6d22c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6d22c-105">タスクのユーザーの進行状況のステータスを指定します。</span><span class="sxs-lookup"><span data-stu-id="6d22c-105">Specifies the status of the user's progress on the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6d22c-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="6d22c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d22c-107">dispidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="6d22c-107">dispidTaskStatus</span></span>  <br/> |
|<span data-ttu-id="6d22c-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6d22c-108">Property set:</span></span>  <br/> |<span data-ttu-id="6d22c-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="6d22c-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="6d22c-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6d22c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6d22c-111">0x00008101</span><span class="sxs-lookup"><span data-stu-id="6d22c-111">0x00008101</span></span>  <br/> |
|<span data-ttu-id="6d22c-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="6d22c-112">Data type:</span></span>  <br/> |<span data-ttu-id="6d22c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6d22c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6d22c-114">領域:</span><span class="sxs-lookup"><span data-stu-id="6d22c-114">Area:</span></span>  <br/> |<span data-ttu-id="6d22c-115">タスク</span><span class="sxs-lookup"><span data-stu-id="6d22c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d22c-116">備考</span><span class="sxs-lookup"><span data-stu-id="6d22c-116">Remarks</span></span>

<span data-ttu-id="6d22c-117">このプロパティの値を次のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d22c-117">The value of this property must be set to one of the following.</span></span>
  
|<span data-ttu-id="6d22c-118">**値**</span><span class="sxs-lookup"><span data-stu-id="6d22c-118">**Value**</span></span>|<span data-ttu-id="6d22c-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="6d22c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d22c-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d22c-120">0x00000000</span></span>  <br/> |<span data-ttu-id="6d22c-121">ユーザーは、タスクの作業を開始されていません。</span><span class="sxs-lookup"><span data-stu-id="6d22c-121">The user has not started work on the task.</span></span> <span data-ttu-id="6d22c-122">この値が設定されている場合、 **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) は、0.0 をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d22c-122">If this value is set, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) must be 0.0.</span></span>  <br/> |
|<span data-ttu-id="6d22c-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6d22c-123">0x00000001</span></span>  <br/> |<span data-ttu-id="6d22c-124">このタスクでのユーザーの作業は進行中です。</span><span class="sxs-lookup"><span data-stu-id="6d22c-124">The user's work on this task is in progress.</span></span> <span data-ttu-id="6d22c-125">この値が設定されている場合、 **dispidPercentComplete**は 0.0 および 1.0 未満の場合よりも大きくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6d22c-125">If this value is set, **dispidPercentComplete** must be greater than 0.0 and less than 1.0.</span></span>  <br/> |
|<span data-ttu-id="6d22c-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6d22c-126">0x00000002</span></span>  <br/> |<span data-ttu-id="6d22c-127">このタスクでのユーザーの作業は完了です。</span><span class="sxs-lookup"><span data-stu-id="6d22c-127">The user's work on this task is complete.</span></span> <span data-ttu-id="6d22c-128">この値が設定されている場合は、 **dispidPercentComplete**は 1.0 である必要があり、 **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) は、現在の日付である必要があります**dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) は TRUE である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d22c-128">If this value is set, **dispidPercentComplete** must be 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) must be the current date, and **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) must be TRUE.</span></span>  <br/> |
|<span data-ttu-id="6d22c-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="6d22c-129">0x00000003</span></span>  <br/> |<span data-ttu-id="6d22c-130">ユーザーは、他のユーザーに待機しています。</span><span class="sxs-lookup"><span data-stu-id="6d22c-130">The user is waiting on somebody else.</span></span>  <br/> |
|<span data-ttu-id="6d22c-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="6d22c-131">0x00000004</span></span>  <br/> |<span data-ttu-id="6d22c-132">ユーザーは、タスクの作業を延期しました。</span><span class="sxs-lookup"><span data-stu-id="6d22c-132">The user has deferred work on the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6d22c-133">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6d22c-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6d22c-134">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6d22c-134">Protocol specifications</span></span>

<span data-ttu-id="6d22c-135">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d22c-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d22c-136">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6d22c-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6d22c-137">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d22c-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d22c-138">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="6d22c-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="6d22c-139">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d22c-139">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d22c-140">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d22c-140">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="6d22c-141">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d22c-141">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d22c-142">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d22c-142">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="6d22c-143">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d22c-143">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d22c-144">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="6d22c-144">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="6d22c-145">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d22c-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d22c-146">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="6d22c-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="6d22c-147">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d22c-147">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d22c-148">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="6d22c-148">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6d22c-149">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6d22c-149">Header files</span></span>

<span data-ttu-id="6d22c-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d22c-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d22c-151">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6d22c-151">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d22c-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="6d22c-152">See also</span></span>



[<span data-ttu-id="6d22c-153">PidLidPercentComplete の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6d22c-153">PidLidPercentComplete Canonical Property</span></span>](pidlidpercentcomplete-canonical-property.md)
  
[<span data-ttu-id="6d22c-154">PidLidTaskDateCompleted の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6d22c-154">PidLidTaskDateCompleted Canonical Property</span></span>](pidlidtaskdatecompleted-canonical-property.md)
  
[<span data-ttu-id="6d22c-155">PidLidTaskComplete の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6d22c-155">PidLidTaskComplete Canonical Property</span></span>](pidlidtaskcomplete-canonical-property.md)


[<span data-ttu-id="6d22c-156">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6d22c-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d22c-157">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6d22c-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d22c-158">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="6d22c-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d22c-159">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="6d22c-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

