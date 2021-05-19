---
title: PidLidForwardInstance 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidForwardInstance
api_type:
- COM
ms.assetid: 055bdcaf-5002-44a6-b2b6-87244b2bea93
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 585e1a5400965288aa4a4c321888a570270021c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357772"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="a770b-103">PidLidForwardInstance 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a770b-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="a770b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a770b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a770b-105">会議出席依頼が定期的なシリーズの例外を表し、開催者から送信された招待ではなく、(開催者によって転送された場合でも) 転送されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a770b-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a770b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a770b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a770b-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="a770b-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="a770b-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="a770b-108">Property set:</span></span>  <br/> |<span data-ttu-id="a770b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a770b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a770b-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a770b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a770b-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="a770b-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="a770b-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a770b-112">Data type:</span></span>  <br/> |<span data-ttu-id="a770b-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a770b-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a770b-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="a770b-114">Area:</span></span>  <br/> |<span data-ttu-id="a770b-115">会議</span><span class="sxs-lookup"><span data-stu-id="a770b-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a770b-116">注釈</span><span class="sxs-lookup"><span data-stu-id="a770b-116">Remarks</span></span>

<span data-ttu-id="a770b-117">このプロパティの値が FALSE の場合は、会議出席依頼が転送されたインスタンスではないかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a770b-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="a770b-118">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="a770b-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a770b-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a770b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a770b-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a770b-120">Protocol specifications</span></span>

<span data-ttu-id="a770b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a770b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a770b-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="a770b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a770b-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a770b-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a770b-124">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a770b-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a770b-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a770b-125">Header files</span></span>

<span data-ttu-id="a770b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a770b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a770b-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a770b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a770b-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="a770b-128">See also</span></span>



[<span data-ttu-id="a770b-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a770b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a770b-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a770b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a770b-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a770b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a770b-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a770b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

