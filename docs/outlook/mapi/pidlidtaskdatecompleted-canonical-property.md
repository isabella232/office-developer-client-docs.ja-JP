---
title: PidLidTaskDateCompleted の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDateCompleted
api_type:
- COM
ms.assetid: ae384529-55e2-4da1-9a41-acc292591a7c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9737b5f940f95c88c2d3c5c6e98fc885daf64219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802175"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a><span data-ttu-id="3d386-103">PidLidTaskDateCompleted の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="3d386-103">PidLidTaskDateCompleted Canonical Property</span></span>

  
  
<span data-ttu-id="3d386-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d386-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d386-105">ユーザーがタスクを完了する日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d386-105">Specifies the date when the user completes the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d386-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="3d386-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d386-107">dispidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="3d386-107">dispidTaskDateCompleted</span></span>  <br/> |
|<span data-ttu-id="3d386-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3d386-108">Property set:</span></span>  <br/> |<span data-ttu-id="3d386-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="3d386-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="3d386-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="3d386-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3d386-111">0x0000810F</span><span class="sxs-lookup"><span data-stu-id="3d386-111">0x0000810F</span></span>  <br/> |
|<span data-ttu-id="3d386-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="3d386-112">Data type:</span></span>  <br/> |<span data-ttu-id="3d386-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3d386-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="3d386-114">領域:</span><span class="sxs-lookup"><span data-stu-id="3d386-114">Area:</span></span>  <br/> |<span data-ttu-id="3d386-115">タスク</span><span class="sxs-lookup"><span data-stu-id="3d386-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d386-116">備考</span><span class="sxs-lookup"><span data-stu-id="3d386-116">Remarks</span></span>

<span data-ttu-id="3d386-117">かどうかこのオプションを設定すると、このプロパティには午前 0 時という時刻成分、ローカル タイム ゾーンで、世界協定時刻 (UTC) への変換します。</span><span class="sxs-lookup"><span data-stu-id="3d386-117">If set, this property must have a time component of midnight in the local time zone, converted to Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3d386-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3d386-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d386-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3d386-119">Protocol specifications</span></span>

<span data-ttu-id="3d386-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d386-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d386-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3d386-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d386-122">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d386-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d386-123">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="3d386-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="3d386-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3d386-124">Header files</span></span>

<span data-ttu-id="3d386-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d386-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d386-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3d386-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d386-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d386-127">See also</span></span>



[<span data-ttu-id="3d386-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d386-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d386-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d386-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d386-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="3d386-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d386-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="3d386-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

