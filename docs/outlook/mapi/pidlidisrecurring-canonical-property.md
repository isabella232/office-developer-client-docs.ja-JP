---
title: PidLidIsRecurring 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c920cd42a27c03ffcff63bbd2e0049ddb6f81158
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315436"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="91f3f-103">PidLidIsRecurring 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91f3f-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="91f3f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91f3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91f3f-105">オブジェクトが定期的な系列に関連付けられているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="91f3f-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91f3f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="91f3f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91f3f-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="91f3f-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="91f3f-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="91f3f-108">Property set:</span></span>  <br/> |<span data-ttu-id="91f3f-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="91f3f-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="91f3f-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="91f3f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="91f3f-111">0x00000005</span><span class="sxs-lookup"><span data-stu-id="91f3f-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="91f3f-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="91f3f-112">Data type:</span></span>  <br/> |<span data-ttu-id="91f3f-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="91f3f-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="91f3f-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="91f3f-114">Area:</span></span>  <br/> |<span data-ttu-id="91f3f-115">会議</span><span class="sxs-lookup"><span data-stu-id="91f3f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91f3f-116">注釈</span><span class="sxs-lookup"><span data-stu-id="91f3f-116">Remarks</span></span>

<span data-ttu-id="91f3f-117">TRUE の値は、オブジェクトが定期的な系列または例外 (孤立したインスタンスを含む) を表します。</span><span class="sxs-lookup"><span data-stu-id="91f3f-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="91f3f-118">FALSE の値、またはこのプロパティがない場合は、オブジェクトが 1 つのインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="91f3f-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="91f3f-119">このプロパティとプロパティ ([PidLidRecurring](pidlidrecurring-canonical-property.md)) **PR_RECURRING** の違いに注意してください。</span><span class="sxs-lookup"><span data-stu-id="91f3f-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="91f3f-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="91f3f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91f3f-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="91f3f-121">Protocol specifications</span></span>

<span data-ttu-id="91f3f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91f3f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91f3f-123">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="91f3f-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91f3f-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91f3f-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91f3f-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="91f3f-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91f3f-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="91f3f-126">Header files</span></span>

<span data-ttu-id="91f3f-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91f3f-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="91f3f-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="91f3f-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91f3f-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="91f3f-129">See also</span></span>



[<span data-ttu-id="91f3f-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="91f3f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91f3f-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91f3f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91f3f-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="91f3f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91f3f-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="91f3f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

