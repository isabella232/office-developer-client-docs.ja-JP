---
title: PidLidPercentComplete 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidPercentComplete
api_type:
- COM
ms.assetid: e63792b1-9580-4702-a6d7-dd3ae5007a4a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 870b4e0edb360ac36525f94b0605af930eee8fa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357975"
---
# <a name="pidlidpercentcomplete-canonical-property"></a><span data-ttu-id="96aee-103">PidLidPercentComplete 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="96aee-103">PidLidPercentComplete Canonical Property</span></span>

  
  
<span data-ttu-id="96aee-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96aee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96aee-105">ユーザーがタスクに対して行った進捗状況を示します。</span><span class="sxs-lookup"><span data-stu-id="96aee-105">Indicates the progress the user has made on a task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96aee-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="96aee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96aee-107">dispidpercentcomplete 率</span><span class="sxs-lookup"><span data-stu-id="96aee-107">dispidPercentComplete</span></span>  <br/> |
|<span data-ttu-id="96aee-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="96aee-108">Property set:</span></span>  <br/> |<span data-ttu-id="96aee-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="96aee-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="96aee-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="96aee-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="96aee-111">0x00008102</span><span class="sxs-lookup"><span data-stu-id="96aee-111">0x00008102</span></span>  <br/> |
|<span data-ttu-id="96aee-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="96aee-112">Data type:</span></span>  <br/> |<span data-ttu-id="96aee-113">PT_R8</span><span class="sxs-lookup"><span data-stu-id="96aee-113">PT_R8</span></span>  <br/> |
|<span data-ttu-id="96aee-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="96aee-114">Area:</span></span>  <br/> |<span data-ttu-id="96aee-115">タスク</span><span class="sxs-lookup"><span data-stu-id="96aee-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96aee-116">解説</span><span class="sxs-lookup"><span data-stu-id="96aee-116">Remarks</span></span>

<span data-ttu-id="96aee-117">このプロパティの値には、0.0 以上で1.0 以下の数値を指定する必要があります。1.0 は作業が完了したことを示し、0.0 は作業が開始されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="96aee-117">The value of this property must be a number greater than or equal to 0.0 and less than or equal to 1.0, where 1.0 indicates that work is completed and 0.0 indicates that work has not begun.</span></span>
  
<span data-ttu-id="96aee-118">タイムフラグが設定されたメッセージオブジェクトの場合、このプロパティの値は、オブジェクトのフラグが設定されている場合は1.0 に設定し、それ以外の場合は0.0 に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96aee-118">For a time-flagged message object, the value of this property must be set to 1.0 if the object is flagged completed, and should be set to 0.0 otherwise.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="96aee-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="96aee-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="96aee-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="96aee-120">Protocol specifications</span></span>

<span data-ttu-id="96aee-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96aee-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96aee-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="96aee-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="96aee-123">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96aee-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96aee-124">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="96aee-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="96aee-125">[[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96aee-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96aee-126">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="96aee-126">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="96aee-127">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96aee-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96aee-128">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="96aee-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="96aee-129">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96aee-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96aee-130">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="96aee-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="96aee-131">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96aee-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96aee-132">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="96aee-132">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="96aee-133">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="96aee-133">Header files</span></span>

<span data-ttu-id="96aee-134">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96aee-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="96aee-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="96aee-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96aee-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="96aee-136">See also</span></span>



[<span data-ttu-id="96aee-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="96aee-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96aee-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="96aee-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96aee-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="96aee-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96aee-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="96aee-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

