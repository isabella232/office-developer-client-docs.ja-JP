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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 149f238ea53e0669f4d95c8e6c2b17a2b5a1c209
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316535"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="b6b55-103">PidLidTaskState 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b6b55-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="b6b55-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6b55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6b55-105">タスクの現在の割り当ての状態を示します。</span><span class="sxs-lookup"><span data-stu-id="b6b55-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6b55-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b6b55-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6b55-107">dispidTaskState</span><span class="sxs-lookup"><span data-stu-id="b6b55-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="b6b55-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="b6b55-108">Property set:</span></span>  <br/> |<span data-ttu-id="b6b55-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b6b55-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b6b55-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b6b55-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b6b55-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="b6b55-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="b6b55-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b6b55-112">Data type:</span></span>  <br/> |<span data-ttu-id="b6b55-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b6b55-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b6b55-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="b6b55-114">Area:</span></span>  <br/> |<span data-ttu-id="b6b55-115">タスク</span><span class="sxs-lookup"><span data-stu-id="b6b55-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6b55-116">注釈</span><span class="sxs-lookup"><span data-stu-id="b6b55-116">Remarks</span></span>

<span data-ttu-id="b6b55-117">このプロパティの値は、次のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6b55-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="b6b55-118">**値**</span><span class="sxs-lookup"><span data-stu-id="b6b55-118">**Value**</span></span>|<span data-ttu-id="b6b55-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="b6b55-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b6b55-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6b55-120">0x00000000</span></span>  <br/> |<span data-ttu-id="b6b55-121">このタスクは、タスク拒否に埋め込まれたタスクに対応するために作成されましたが、ローカルで見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="b6b55-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="b6b55-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b6b55-122">0x00000001</span></span>  <br/> |<span data-ttu-id="b6b55-123">タスクが割り当てられていない。</span><span class="sxs-lookup"><span data-stu-id="b6b55-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="b6b55-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b6b55-124">0x00000002</span></span>  <br/> |<span data-ttu-id="b6b55-125">タスクは、割り当てられたタスクのタスクの割り当て先のコピーです。</span><span class="sxs-lookup"><span data-stu-id="b6b55-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="b6b55-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b6b55-126">0x00000003</span></span>  <br/> |<span data-ttu-id="b6b55-127">タスクは、割り当てられたタスクのタスク割り当て者のコピーです。</span><span class="sxs-lookup"><span data-stu-id="b6b55-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="b6b55-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b6b55-128">0x00000004</span></span>  <br/> |<span data-ttu-id="b6b55-129">タスクは、拒否されたタスクのタスク割り当て者のコピーです。</span><span class="sxs-lookup"><span data-stu-id="b6b55-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b6b55-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b6b55-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b6b55-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b6b55-131">Protocol specifications</span></span>

<span data-ttu-id="b6b55-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6b55-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6b55-133">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="b6b55-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b6b55-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6b55-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6b55-135">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="b6b55-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="b6b55-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6b55-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6b55-137">メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b6b55-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="b6b55-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6b55-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6b55-139">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="b6b55-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b6b55-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6b55-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6b55-141">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="b6b55-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b6b55-142">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b6b55-142">Header files</span></span>

<span data-ttu-id="b6b55-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6b55-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6b55-144">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b6b55-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6b55-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6b55-145">See also</span></span>



[<span data-ttu-id="b6b55-146">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b6b55-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6b55-147">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b6b55-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6b55-148">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b6b55-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6b55-149">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b6b55-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

