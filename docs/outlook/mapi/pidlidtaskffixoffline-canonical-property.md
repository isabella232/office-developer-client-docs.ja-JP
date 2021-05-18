---
title: PidLidTaskFFixOffline 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 226e59ef6aa88bc290cf5aeb4d620979f926e1eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303039"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="577ed-103">PidLidTaskFFixOffline 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="577ed-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="577ed-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="577ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="577ed-105">**dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) プロパティの精度を示します。</span><span class="sxs-lookup"><span data-stu-id="577ed-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="577ed-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="577ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="577ed-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="577ed-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="577ed-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="577ed-108">Property set:</span></span>  <br/> |<span data-ttu-id="577ed-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="577ed-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="577ed-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="577ed-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="577ed-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="577ed-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="577ed-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="577ed-112">Data type:</span></span>  <br/> |<span data-ttu-id="577ed-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="577ed-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="577ed-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="577ed-114">Area:</span></span>  <br/> |<span data-ttu-id="577ed-115">タスク</span><span class="sxs-lookup"><span data-stu-id="577ed-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="577ed-116">注釈</span><span class="sxs-lookup"><span data-stu-id="577ed-116">Remarks</span></span>

<span data-ttu-id="577ed-117">**dispidTaskFFixOffline** プロパティが FALSE に設定されている場合、または設定されていない場合 **、dispidTaskOwner** プロパティの値は正しいです。</span><span class="sxs-lookup"><span data-stu-id="577ed-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="577ed-118">**dispidTaskFFixOffline** が TRUE に設定されている場合、クライアントは **dispidTaskOwner** の正確な値を判断できません。</span><span class="sxs-lookup"><span data-stu-id="577ed-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="577ed-119">その場合、クライアントは **dispidTaskOwner** を "不明" などの一般的な所有者名に設定できます。</span><span class="sxs-lookup"><span data-stu-id="577ed-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="577ed-120">ただし、クライアントで **dispidTaskFFixOffline** 値が TRUE に検出され、正確な所有者名を特定できる場合、クライアントは **dispidTaskOwner を更新し、dispidTaskFFixOffline** を FALSE に設定する必要があります。 </span><span class="sxs-lookup"><span data-stu-id="577ed-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="577ed-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="577ed-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="577ed-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="577ed-122">Protocol specifications</span></span>

<span data-ttu-id="577ed-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="577ed-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="577ed-124">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="577ed-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="577ed-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="577ed-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="577ed-126">タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="577ed-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="577ed-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="577ed-127">Header files</span></span>

<span data-ttu-id="577ed-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="577ed-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="577ed-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="577ed-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="577ed-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="577ed-130">See also</span></span>



[<span data-ttu-id="577ed-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="577ed-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="577ed-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="577ed-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="577ed-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="577ed-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="577ed-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="577ed-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

