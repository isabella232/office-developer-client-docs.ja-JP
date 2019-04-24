---
title: PidLidTaskLastUpdate 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 95af98acad6b2aa4bc95ea5e6478e6ca21c8eb8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356834"
---
# <a name="pidlidtasklastupdate-canonical-property"></a><span data-ttu-id="5ed92-103">PidLidTaskLastUpdate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5ed92-103">PidLidTaskLastUpdate Canonical Property</span></span>

  
  
<span data-ttu-id="5ed92-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ed92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ed92-105">**dispidTaskHistory** ([PidLidTaskHistory](pidlidtasklastupdate-canonical-property.md)) プロパティで示される、タスクに対して行われた最新の変更の世界協定時刻 (UTC) と日付を示します。</span><span class="sxs-lookup"><span data-stu-id="5ed92-105">Indicates the Coordinated Universal Time (UTC) and date of the most recent change that was made to the task and indicated by the **dispidTaskHistory** ([PidLidTaskHistory](pidlidtasklastupdate-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ed92-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5ed92-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ed92-107">dispidtasklastupdate</span><span class="sxs-lookup"><span data-stu-id="5ed92-107">dispidTaskLastUpdate</span></span>  <br/> |
|<span data-ttu-id="5ed92-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="5ed92-108">Property set:</span></span>  <br/> |<span data-ttu-id="5ed92-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="5ed92-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="5ed92-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5ed92-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5ed92-111">0x00008115</span><span class="sxs-lookup"><span data-stu-id="5ed92-111">0x00008115</span></span>  <br/> |
|<span data-ttu-id="5ed92-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5ed92-112">Data type:</span></span>  <br/> |<span data-ttu-id="5ed92-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5ed92-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5ed92-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="5ed92-114">Area:</span></span>  <br/> |<span data-ttu-id="5ed92-115">タスク</span><span class="sxs-lookup"><span data-stu-id="5ed92-115">Task</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5ed92-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5ed92-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5ed92-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5ed92-117">Protocol specifications</span></span>

<span data-ttu-id="5ed92-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ed92-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ed92-119">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5ed92-119">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5ed92-120">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ed92-120">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ed92-121">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="5ed92-121">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5ed92-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="5ed92-122">Header files</span></span>

<span data-ttu-id="5ed92-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ed92-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ed92-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5ed92-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ed92-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ed92-125">See also</span></span>



[<span data-ttu-id="5ed92-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5ed92-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ed92-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5ed92-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ed92-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5ed92-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ed92-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5ed92-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

