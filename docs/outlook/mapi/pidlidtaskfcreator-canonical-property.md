---
title: PidLidTaskFCreator の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFCreator
api_type:
- COM
ms.assetid: bb88750b-4773-4241-aa38-462a2634dbcb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 458a20e238d6023520ede3416ece239f2d553891
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802211"
---
# <a name="pidlidtaskfcreator-canonical-property"></a><span data-ttu-id="7bdde-103">PidLidTaskFCreator の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7bdde-103">PidLidTaskFCreator Canonical Property</span></span>

  
  
<span data-ttu-id="7bdde-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7bdde-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7bdde-105">仕事の依頼を処理することによって、現在のユーザーまたはユーザー ・ エージェントの代わりに、タスクの作成元を示します。</span><span class="sxs-lookup"><span data-stu-id="7bdde-105">Indicates the task was originally created by the current user or user agent instead of by processing a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7bdde-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7bdde-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7bdde-107">dispidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="7bdde-107">dispidTaskFCreator</span></span>  <br/> |
|<span data-ttu-id="7bdde-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7bdde-108">Property set:</span></span>  <br/> |<span data-ttu-id="7bdde-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="7bdde-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="7bdde-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7bdde-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7bdde-111">0x0000811E</span><span class="sxs-lookup"><span data-stu-id="7bdde-111">0x0000811E</span></span>  <br/> |
|<span data-ttu-id="7bdde-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="7bdde-112">Data type:</span></span>  <br/> |<span data-ttu-id="7bdde-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7bdde-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7bdde-114">領域:</span><span class="sxs-lookup"><span data-stu-id="7bdde-114">Area:</span></span>  <br/> |<span data-ttu-id="7bdde-115">タスク</span><span class="sxs-lookup"><span data-stu-id="7bdde-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bdde-116">備考</span><span class="sxs-lookup"><span data-stu-id="7bdde-116">Remarks</span></span>

<span data-ttu-id="7bdde-117">クライアントこのプロパティ設定をユーザーがタスクを作成するときに TRUE と false を指定する別のユーザーによって、タスクが割り当てられている場合。</span><span class="sxs-lookup"><span data-stu-id="7bdde-117">The client sets this property to TRUE when the user creates the task and to FALSE when the task is assigned by another user.</span></span> <span data-ttu-id="7bdde-118">このプロパティが未設定のままには、TRUE の値が使われます。</span><span class="sxs-lookup"><span data-stu-id="7bdde-118">If this property is left unset, a value of TRUE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7bdde-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7bdde-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7bdde-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7bdde-120">Protocol specifications</span></span>

<span data-ttu-id="7bdde-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7bdde-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7bdde-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7bdde-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7bdde-123">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7bdde-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7bdde-124">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="7bdde-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7bdde-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7bdde-125">Header files</span></span>

<span data-ttu-id="7bdde-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7bdde-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7bdde-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7bdde-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7bdde-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="7bdde-128">See also</span></span>



[<span data-ttu-id="7bdde-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7bdde-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7bdde-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7bdde-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7bdde-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7bdde-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7bdde-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="7bdde-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

