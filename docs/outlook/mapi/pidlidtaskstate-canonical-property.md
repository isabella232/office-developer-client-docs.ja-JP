---
title: PidLidTaskState 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskState
api_type:
- COM
ms.assetid: 06d1f8a3-53e1-4c9a-9703-75de7a11a772
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 149f238ea53e0669f4d95c8e6c2b17a2b5a1c209
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316535"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="9f78a-103">PidLidTaskState 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9f78a-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="9f78a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f78a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f78a-105">タスクの現在の割り当て状態を示します。</span><span class="sxs-lookup"><span data-stu-id="9f78a-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f78a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9f78a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f78a-107">dispidtaskstate</span><span class="sxs-lookup"><span data-stu-id="9f78a-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="9f78a-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="9f78a-108">Property set:</span></span>  <br/> |<span data-ttu-id="9f78a-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="9f78a-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="9f78a-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9f78a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9f78a-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="9f78a-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="9f78a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9f78a-112">Data type:</span></span>  <br/> |<span data-ttu-id="9f78a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9f78a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9f78a-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="9f78a-114">Area:</span></span>  <br/> |<span data-ttu-id="9f78a-115">タスク</span><span class="sxs-lookup"><span data-stu-id="9f78a-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f78a-116">解説</span><span class="sxs-lookup"><span data-stu-id="9f78a-116">Remarks</span></span>

<span data-ttu-id="9f78a-117">このプロパティの値は、次のいずれかであることが必要です。</span><span class="sxs-lookup"><span data-stu-id="9f78a-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="9f78a-118">**値**</span><span class="sxs-lookup"><span data-stu-id="9f78a-118">**Value**</span></span>|<span data-ttu-id="9f78a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="9f78a-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9f78a-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f78a-120">0x00000000</span></span>  <br/> |<span data-ttu-id="9f78a-121">このタスクは、タスクの却下に埋め込まれているが、ローカルでは見つからないタスクに対応するために作成されました。</span><span class="sxs-lookup"><span data-stu-id="9f78a-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="9f78a-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9f78a-122">0x00000001</span></span>  <br/> |<span data-ttu-id="9f78a-123">タスクが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="9f78a-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="9f78a-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9f78a-124">0x00000002</span></span>  <br/> |<span data-ttu-id="9f78a-125">タスクは、割り当てられたタスクのタスク実施者のコピーです。</span><span class="sxs-lookup"><span data-stu-id="9f78a-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="9f78a-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="9f78a-126">0x00000003</span></span>  <br/> |<span data-ttu-id="9f78a-127">タスクは、割り当てられたタスクのタスク assigner のコピーです。</span><span class="sxs-lookup"><span data-stu-id="9f78a-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="9f78a-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9f78a-128">0x00000004</span></span>  <br/> |<span data-ttu-id="9f78a-129">タスクは、却下されたタスクのタスク assigner のコピーです。</span><span class="sxs-lookup"><span data-stu-id="9f78a-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9f78a-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9f78a-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9f78a-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9f78a-131">Protocol specifications</span></span>

<span data-ttu-id="9f78a-132">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f78a-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f78a-133">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9f78a-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9f78a-134">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f78a-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f78a-135">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="9f78a-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="9f78a-136">[[OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f78a-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f78a-137">メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9f78a-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="9f78a-138">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f78a-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f78a-139">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="9f78a-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="9f78a-140">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f78a-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f78a-141">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="9f78a-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9f78a-142">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9f78a-142">Header files</span></span>

<span data-ttu-id="9f78a-143">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f78a-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f78a-144">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9f78a-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f78a-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="9f78a-145">See also</span></span>



[<span data-ttu-id="9f78a-146">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9f78a-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f78a-147">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9f78a-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f78a-148">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9f78a-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f78a-149">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9f78a-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

