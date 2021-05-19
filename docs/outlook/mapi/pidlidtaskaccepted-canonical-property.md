---
title: PidLidTaskAccepted 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAccepted
api_type:
- COM
ms.assetid: 8e31f893-b639-43da-a535-662153c82d82
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0172bf0d69c3f345b592364be754f58c9e7a4420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331284"
---
# <a name="pidlidtaskaccepted-canonical-property"></a><span data-ttu-id="876ea-103">PidLidTaskAccepted 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="876ea-103">PidLidTaskAccepted Canonical Property</span></span>

  
  
<span data-ttu-id="876ea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="876ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="876ea-105">タスクの割り当て先がタスク要求に返信したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="876ea-105">Indicates whether a task assignee has replied to a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="876ea-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="876ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="876ea-107">dispidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="876ea-107">dispidTaskAccepted</span></span>  <br/> |
|<span data-ttu-id="876ea-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="876ea-108">Property set:</span></span>  <br/> |<span data-ttu-id="876ea-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="876ea-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="876ea-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="876ea-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="876ea-111">0x00008108</span><span class="sxs-lookup"><span data-stu-id="876ea-111">0x00008108</span></span>  <br/> |
|<span data-ttu-id="876ea-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="876ea-112">Data type:</span></span>  <br/> |<span data-ttu-id="876ea-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="876ea-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="876ea-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="876ea-114">Area:</span></span>  <br/> |<span data-ttu-id="876ea-115">タスク</span><span class="sxs-lookup"><span data-stu-id="876ea-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="876ea-116">注釈</span><span class="sxs-lookup"><span data-stu-id="876ea-116">Remarks</span></span>

<span data-ttu-id="876ea-117">クライアントは、新しいタスクに対してこのプロパティを FALSE に設定するか、タスクが受け入れられるか拒否された場合に、このプロパティを TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="876ea-117">The client sets this property to FALSE for a new task, or the client sets this property to TRUE when a task is either accepted or rejected.</span></span> <span data-ttu-id="876ea-118">プロパティが設定されていない場合は、FALSE の値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="876ea-118">If the property is left unset, a value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="876ea-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="876ea-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="876ea-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="876ea-120">Protocol specifications</span></span>

<span data-ttu-id="876ea-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="876ea-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="876ea-122">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="876ea-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="876ea-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="876ea-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="876ea-124">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="876ea-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="876ea-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="876ea-125">Header files</span></span>

<span data-ttu-id="876ea-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="876ea-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="876ea-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="876ea-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="876ea-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="876ea-128">See also</span></span>



[<span data-ttu-id="876ea-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="876ea-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="876ea-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="876ea-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="876ea-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="876ea-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="876ea-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="876ea-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

