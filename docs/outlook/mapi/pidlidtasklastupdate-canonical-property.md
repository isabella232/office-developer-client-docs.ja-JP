---
title: PidLidTaskLastUpdate の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUpdate
api_type:
- COM
ms.assetid: 65b73d0f-f1f1-4c11-8834-f7c736a30ffc
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: acd06027f1f9aa051a36192f07efa3ca0671a82e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802215"
---
# <a name="pidlidtasklastupdate-canonical-property"></a><span data-ttu-id="b7040-103">PidLidTaskLastUpdate の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b7040-103">PidLidTaskLastUpdate Canonical Property</span></span>

  
  
<span data-ttu-id="b7040-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7040-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7040-105">世界協定時刻 (UTC) と、タスクに加えられたおよび**dispidTaskHistory** ([PidLidTaskHistory](pidlidtasklastupdate-canonical-property.md)) のプロパティで示された最新の変更の日付を示します。</span><span class="sxs-lookup"><span data-stu-id="b7040-105">Indicates the Coordinated Universal Time (UTC) and date of the most recent change that was made to the task and indicated by the **dispidTaskHistory** ([PidLidTaskHistory](pidlidtasklastupdate-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7040-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b7040-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7040-107">dispidTaskLastUpdate</span><span class="sxs-lookup"><span data-stu-id="b7040-107">dispidTaskLastUpdate</span></span>  <br/> |
|<span data-ttu-id="b7040-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b7040-108">Property set:</span></span>  <br/> |<span data-ttu-id="b7040-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b7040-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b7040-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b7040-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b7040-111">0x00008115</span><span class="sxs-lookup"><span data-stu-id="b7040-111">0x00008115</span></span>  <br/> |
|<span data-ttu-id="b7040-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="b7040-112">Data type:</span></span>  <br/> |<span data-ttu-id="b7040-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b7040-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b7040-114">領域:</span><span class="sxs-lookup"><span data-stu-id="b7040-114">Area:</span></span>  <br/> |<span data-ttu-id="b7040-115">タスク</span><span class="sxs-lookup"><span data-stu-id="b7040-115">Task</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b7040-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b7040-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7040-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b7040-117">Protocol specifications</span></span>

<span data-ttu-id="b7040-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7040-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7040-119">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7040-119">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7040-120">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7040-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7040-121">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="b7040-121">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7040-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b7040-122">Header files</span></span>

<span data-ttu-id="b7040-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7040-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7040-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7040-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7040-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7040-125">See also</span></span>



[<span data-ttu-id="b7040-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7040-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7040-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7040-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7040-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="b7040-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7040-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="b7040-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

