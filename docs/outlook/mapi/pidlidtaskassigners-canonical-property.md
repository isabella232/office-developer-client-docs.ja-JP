---
title: PidLidTaskAssigners の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 89e0b6eae35de9e40dba411afb82e19aa81fb635
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802183"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="8d23a-103">PidLidTaskAssigners の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8d23a-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="8d23a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8d23a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8d23a-105">タスク assigners を表すエントリのスタックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d23a-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="8d23a-106">最新作業仕事を割り当てた人は、スタックの一番上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="8d23a-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d23a-107">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="8d23a-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d23a-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="8d23a-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="8d23a-109">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8d23a-109">Property set:</span></span>  <br/> |<span data-ttu-id="8d23a-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="8d23a-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="8d23a-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8d23a-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8d23a-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="8d23a-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="8d23a-113">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="8d23a-113">Data type:</span></span>  <br/> |<span data-ttu-id="8d23a-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8d23a-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8d23a-115">領域:</span><span class="sxs-lookup"><span data-stu-id="8d23a-115">Area:</span></span>  <br/> |<span data-ttu-id="8d23a-116">タスク</span><span class="sxs-lookup"><span data-stu-id="8d23a-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d23a-117">備考</span><span class="sxs-lookup"><span data-stu-id="8d23a-117">Remarks</span></span>

<span data-ttu-id="8d23a-118">クライアントでは、仕事の依頼を受信すると、 [[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)、タスクの送信者を表すエントリにどのような構造が定義されている、このプロパティに追加します。</span><span class="sxs-lookup"><span data-stu-id="8d23a-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="8d23a-119">クライアントは、タスクの辞退を受信すると、クライアントは、このプロパティからタスクの最後の仕事を割り当てた人エントリを削除します。</span><span class="sxs-lookup"><span data-stu-id="8d23a-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="8d23a-120">クライアントは、タスクの応答を送信するクライアントは、前回作業仕事を割り当てた人にこのプロパティの値を一覧表示するに送信します。</span><span class="sxs-lookup"><span data-stu-id="8d23a-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8d23a-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8d23a-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d23a-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8d23a-122">Protocol specifications</span></span>

<span data-ttu-id="8d23a-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d23a-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d23a-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8d23a-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8d23a-125">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d23a-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d23a-126">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="8d23a-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="8d23a-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8d23a-127">Header files</span></span>

<span data-ttu-id="8d23a-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d23a-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d23a-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8d23a-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d23a-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d23a-130">See also</span></span>



[<span data-ttu-id="8d23a-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d23a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d23a-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d23a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d23a-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="8d23a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d23a-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="8d23a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

