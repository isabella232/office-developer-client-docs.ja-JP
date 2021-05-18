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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d058b42ad7d1a1b8387aa5b9a1a65ea160d90b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316668"
---
# <a name="pidlidtaskstatus-canonical-property"></a><span data-ttu-id="58fde-103">PidLidTaskStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="58fde-103">PidLidTaskStatus Canonical Property</span></span>

  
  
<span data-ttu-id="58fde-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58fde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58fde-105">タスクのユーザーの進行状況の状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="58fde-105">Specifies the status of the user's progress on the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58fde-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="58fde-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58fde-107">dispidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="58fde-107">dispidTaskStatus</span></span>  <br/> |
|<span data-ttu-id="58fde-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="58fde-108">Property set:</span></span>  <br/> |<span data-ttu-id="58fde-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="58fde-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="58fde-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="58fde-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="58fde-111">0x00008101</span><span class="sxs-lookup"><span data-stu-id="58fde-111">0x00008101</span></span>  <br/> |
|<span data-ttu-id="58fde-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="58fde-112">Data type:</span></span>  <br/> |<span data-ttu-id="58fde-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="58fde-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="58fde-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="58fde-114">Area:</span></span>  <br/> |<span data-ttu-id="58fde-115">タスク</span><span class="sxs-lookup"><span data-stu-id="58fde-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58fde-116">注釈</span><span class="sxs-lookup"><span data-stu-id="58fde-116">Remarks</span></span>

<span data-ttu-id="58fde-117">このプロパティの値は、次のいずれかの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58fde-117">The value of this property must be set to one of the following.</span></span>
  
|<span data-ttu-id="58fde-118">**値**</span><span class="sxs-lookup"><span data-stu-id="58fde-118">**Value**</span></span>|<span data-ttu-id="58fde-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="58fde-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58fde-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58fde-120">0x00000000</span></span>  <br/> |<span data-ttu-id="58fde-121">ユーザーがタスクの作業を開始していない。</span><span class="sxs-lookup"><span data-stu-id="58fde-121">The user has not started work on the task.</span></span> <span data-ttu-id="58fde-122">この値を設定する場合 **、dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) は 0.0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="58fde-122">If this value is set, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) must be 0.0.</span></span>  <br/> |
|<span data-ttu-id="58fde-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="58fde-123">0x00000001</span></span>  <br/> |<span data-ttu-id="58fde-124">このタスクに関するユーザーの作業が進行中です。</span><span class="sxs-lookup"><span data-stu-id="58fde-124">The user's work on this task is in progress.</span></span> <span data-ttu-id="58fde-125">この値を設定する場合 **、dispidPercentComplete** は 0.0 より大きく、1.0 未満である必要があります。</span><span class="sxs-lookup"><span data-stu-id="58fde-125">If this value is set, **dispidPercentComplete** must be greater than 0.0 and less than 1.0.</span></span>  <br/> |
|<span data-ttu-id="58fde-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="58fde-126">0x00000002</span></span>  <br/> |<span data-ttu-id="58fde-127">このタスクに関するユーザーの作業が完了しました。</span><span class="sxs-lookup"><span data-stu-id="58fde-127">The user's work on this task is complete.</span></span> <span data-ttu-id="58fde-128">この値を設定する場合 **、dispidPercentComplete** は 1.0、dispidTaskDateCompleted ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) は現在の日付で **、dispidTaskComplete** (  [PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) は TRUE である必要があります。</span><span class="sxs-lookup"><span data-stu-id="58fde-128">If this value is set, **dispidPercentComplete** must be 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) must be the current date, and **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) must be TRUE.</span></span>  <br/> |
|<span data-ttu-id="58fde-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="58fde-129">0x00000003</span></span>  <br/> |<span data-ttu-id="58fde-130">ユーザーが他のユーザーを待機しています。</span><span class="sxs-lookup"><span data-stu-id="58fde-130">The user is waiting on somebody else.</span></span>  <br/> |
|<span data-ttu-id="58fde-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="58fde-131">0x00000004</span></span>  <br/> |<span data-ttu-id="58fde-132">ユーザーがタスクの作業を延期しました。</span><span class="sxs-lookup"><span data-stu-id="58fde-132">The user has deferred work on the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="58fde-133">関連リソース</span><span class="sxs-lookup"><span data-stu-id="58fde-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58fde-134">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="58fde-134">Protocol specifications</span></span>

<span data-ttu-id="58fde-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58fde-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58fde-136">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="58fde-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58fde-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58fde-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58fde-138">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="58fde-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="58fde-139">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58fde-139">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58fde-140">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="58fde-140">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="58fde-141">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58fde-141">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58fde-142">メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="58fde-142">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="58fde-143">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58fde-143">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58fde-144">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="58fde-144">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="58fde-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58fde-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58fde-146">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="58fde-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="58fde-147">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58fde-147">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58fde-148">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="58fde-148">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58fde-149">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="58fde-149">Header files</span></span>

<span data-ttu-id="58fde-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58fde-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="58fde-151">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="58fde-151">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58fde-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="58fde-152">See also</span></span>



[<span data-ttu-id="58fde-153">PidLidPercentComplete 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="58fde-153">PidLidPercentComplete Canonical Property</span></span>](pidlidpercentcomplete-canonical-property.md)
  
[<span data-ttu-id="58fde-154">PidLidTaskDateCompleted 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="58fde-154">PidLidTaskDateCompleted Canonical Property</span></span>](pidlidtaskdatecompleted-canonical-property.md)
  
[<span data-ttu-id="58fde-155">PidLidTaskComplete 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="58fde-155">PidLidTaskComplete Canonical Property</span></span>](pidlidtaskcomplete-canonical-property.md)


[<span data-ttu-id="58fde-156">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="58fde-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58fde-157">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="58fde-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58fde-158">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="58fde-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58fde-159">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="58fde-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

