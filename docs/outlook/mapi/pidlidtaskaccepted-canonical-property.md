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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 08ea83a12b1c5751ed66643eaacd9bbdd261ff19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579005"
---
# <a name="pidlidtaskaccepted-canonical-property"></a><span data-ttu-id="04af5-103">PidLidTaskAccepted 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="04af5-103">PidLidTaskAccepted Canonical Property</span></span>

  
  
<span data-ttu-id="04af5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04af5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04af5-105">タスクの実施者が仕事の依頼に返信されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="04af5-105">Indicates whether a task assignee has replied to a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04af5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="04af5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04af5-107">dispidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="04af5-107">dispidTaskAccepted</span></span>  <br/> |
|<span data-ttu-id="04af5-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="04af5-108">Property set:</span></span>  <br/> |<span data-ttu-id="04af5-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="04af5-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="04af5-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="04af5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="04af5-111">0x00008108</span><span class="sxs-lookup"><span data-stu-id="04af5-111">0x00008108</span></span>  <br/> |
|<span data-ttu-id="04af5-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="04af5-112">Data type:</span></span>  <br/> |<span data-ttu-id="04af5-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="04af5-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="04af5-114">領域:</span><span class="sxs-lookup"><span data-stu-id="04af5-114">Area:</span></span>  <br/> |<span data-ttu-id="04af5-115">タスク</span><span class="sxs-lookup"><span data-stu-id="04af5-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04af5-116">注釈</span><span class="sxs-lookup"><span data-stu-id="04af5-116">Remarks</span></span>

<span data-ttu-id="04af5-117">クライアントは、タスクには、FALSE にこのプロパティを設定またはタスクが承諾または却下すると、クライアントが TRUE にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="04af5-117">The client sets this property to FALSE for a new task, or the client sets this property to TRUE when a task is either accepted or rejected.</span></span> <span data-ttu-id="04af5-118">プロパティが未設定のままには、FALSE の値が使われます。</span><span class="sxs-lookup"><span data-stu-id="04af5-118">If the property is left unset, a value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="04af5-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="04af5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="04af5-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="04af5-120">Protocol specifications</span></span>

<span data-ttu-id="04af5-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04af5-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04af5-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="04af5-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="04af5-123">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04af5-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04af5-124">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="04af5-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="04af5-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="04af5-125">Header files</span></span>

<span data-ttu-id="04af5-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04af5-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="04af5-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="04af5-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04af5-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="04af5-128">See also</span></span>



[<span data-ttu-id="04af5-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="04af5-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04af5-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="04af5-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04af5-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="04af5-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04af5-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="04af5-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

