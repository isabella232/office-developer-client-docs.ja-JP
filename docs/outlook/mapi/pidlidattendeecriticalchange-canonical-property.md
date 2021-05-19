---
title: PidLidAttendeeCriticalChange 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAttendeeCriticalChange
api_type:
- COM
ms.assetid: 2b46966d-c63d-4241-92d4-001d6a674e97
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d6464a346d8543a128ec1af9f605667c6a51ca3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342043"
---
# <a name="pidlidattendeecriticalchange-canonical-property"></a><span data-ttu-id="c4bd2-103">PidLidAttendeeCriticalChange 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4bd2-103">PidLidAttendeeCriticalChange Canonical Property</span></span>

  
  
<span data-ttu-id="c4bd2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4bd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4bd2-105">会議関連オブジェクトが送信された日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-105">Specifies the date and time when the meeting-related object was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4bd2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c4bd2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4bd2-107">LID_ATTENDEE_CRITICAL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="c4bd2-107">LID_ATTENDEE_CRITICAL_CHANGE</span></span>  <br/> |
|<span data-ttu-id="c4bd2-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="c4bd2-108">Property set:</span></span>  <br/> |<span data-ttu-id="c4bd2-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="c4bd2-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="c4bd2-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c4bd2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c4bd2-111">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c4bd2-111">0x00000001</span></span>  <br/> |
|<span data-ttu-id="c4bd2-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c4bd2-112">Data type:</span></span>  <br/> |<span data-ttu-id="c4bd2-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c4bd2-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c4bd2-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="c4bd2-114">Area:</span></span>  <br/> |<span data-ttu-id="c4bd2-115">会議</span><span class="sxs-lookup"><span data-stu-id="c4bd2-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4bd2-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c4bd2-116">Remarks</span></span>

<span data-ttu-id="c4bd2-117">値は協定世界時 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c4bd2-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c4bd2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4bd2-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c4bd2-119">Protocol specifications</span></span>

<span data-ttu-id="c4bd2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4bd2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4bd2-121">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c4bd2-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4bd2-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4bd2-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4bd2-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c4bd2-124">Header files</span></span>

<span data-ttu-id="c4bd2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4bd2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4bd2-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4bd2-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c4bd2-127">See also</span></span>



[<span data-ttu-id="c4bd2-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c4bd2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4bd2-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4bd2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4bd2-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c4bd2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4bd2-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c4bd2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

