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
ms.openlocfilehash: f4675362de1e9efe4ef16285723cddeface9c403
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802091"
---
# <a name="pidlidpercentcomplete-canonical-property"></a><span data-ttu-id="d107b-103">PidLidPercentComplete 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d107b-103">PidLidPercentComplete Canonical Property</span></span>

  
  
<span data-ttu-id="d107b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d107b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d107b-105">タスクの進行状況のユーザーが行ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="d107b-105">Indicates the progress the user has made on a task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d107b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d107b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d107b-107">dispidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="d107b-107">dispidPercentComplete</span></span>  <br/> |
|<span data-ttu-id="d107b-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d107b-108">Property set:</span></span>  <br/> |<span data-ttu-id="d107b-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="d107b-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="d107b-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d107b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d107b-111">0x00008102</span><span class="sxs-lookup"><span data-stu-id="d107b-111">0x00008102</span></span>  <br/> |
|<span data-ttu-id="d107b-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d107b-112">Data type:</span></span>  <br/> |<span data-ttu-id="d107b-113">PT_R8</span><span class="sxs-lookup"><span data-stu-id="d107b-113">PT_R8</span></span>  <br/> |
|<span data-ttu-id="d107b-114">領域:</span><span class="sxs-lookup"><span data-stu-id="d107b-114">Area:</span></span>  <br/> |<span data-ttu-id="d107b-115">タスク</span><span class="sxs-lookup"><span data-stu-id="d107b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d107b-116">注釈</span><span class="sxs-lookup"><span data-stu-id="d107b-116">Remarks</span></span>

<span data-ttu-id="d107b-117">このプロパティの値は、0.0 以上の番号をする必要があり、作業が開始されていないことを示すよりも 1.0、1.0 が作業が完了したことを示す位置に、かつ、0.0 未満です。</span><span class="sxs-lookup"><span data-stu-id="d107b-117">The value of this property must be a number greater than or equal to 0.0 and less than or equal to 1.0, where 1.0 indicates that work is completed and 0.0 indicates that work has not begun.</span></span>
  
<span data-ttu-id="d107b-118">時間フラグ付きメッセージをオブジェクトでは、このプロパティの値をする必要があるに設定 1.0 オブジェクトのフラグが設定されている場合完了すると、それ以外の場合に 0.0 に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d107b-118">For a time-flagged message object, the value of this property must be set to 1.0 if the object is flagged completed, and should be set to 0.0 otherwise.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d107b-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d107b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d107b-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d107b-120">Protocol specifications</span></span>

<span data-ttu-id="d107b-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d107b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d107b-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d107b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d107b-123">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d107b-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d107b-124">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="d107b-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="d107b-125">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d107b-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d107b-126">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d107b-126">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="d107b-127">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d107b-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d107b-128">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="d107b-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="d107b-129">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d107b-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d107b-130">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="d107b-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="d107b-131">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d107b-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d107b-132">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="d107b-132">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d107b-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d107b-133">Header files</span></span>

<span data-ttu-id="d107b-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d107b-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="d107b-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d107b-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d107b-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="d107b-136">See also</span></span>



[<span data-ttu-id="d107b-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d107b-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d107b-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d107b-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d107b-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d107b-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d107b-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d107b-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

