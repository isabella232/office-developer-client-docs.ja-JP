---
title: PidLidBusyStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusyStatus
api_type:
- COM
ms.assetid: 50c91fe6-2a61-4348-a16d-fd5c501b0715
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cb73a0e09436177b8b53a05588508886ee28a0a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342029"
---
# <a name="pidlidbusystatus-canonical-property"></a><span data-ttu-id="bf1eb-103">PidLidBusyStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bf1eb-103">PidLidBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="bf1eb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf1eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf1eb-105">予定に対するユーザーの空き時間情報を表します。</span><span class="sxs-lookup"><span data-stu-id="bf1eb-105">Represents the user's availability for an appointment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf1eb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bf1eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf1eb-107">dispidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="bf1eb-107">dispidBusyStatus</span></span>  <br/> |
|<span data-ttu-id="bf1eb-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="bf1eb-108">Property set:</span></span>  <br/> |<span data-ttu-id="bf1eb-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="bf1eb-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="bf1eb-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bf1eb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bf1eb-111">0x00008205</span><span class="sxs-lookup"><span data-stu-id="bf1eb-111">0x00008205</span></span>  <br/> |
|<span data-ttu-id="bf1eb-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bf1eb-112">Data type:</span></span>  <br/> |<span data-ttu-id="bf1eb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bf1eb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bf1eb-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="bf1eb-114">Area:</span></span>  <br/> |<span data-ttu-id="bf1eb-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="bf1eb-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf1eb-116">注釈</span><span class="sxs-lookup"><span data-stu-id="bf1eb-116">Remarks</span></span>

<span data-ttu-id="bf1eb-117">このプロパティは、オブジェクトによって記述されるイベントに対するユーザーの可用性を指定し、以下に指定する値の 1 つである必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf1eb-117">This property specifies the availability of a user for the event described by the object and must be one of the values specified below.</span></span>
  
|<span data-ttu-id="bf1eb-118">**値**</span><span class="sxs-lookup"><span data-stu-id="bf1eb-118">**Value**</span></span>|<span data-ttu-id="bf1eb-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="bf1eb-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bf1eb-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf1eb-120">0x00000000</span></span>  <br/> |<span data-ttu-id="bf1eb-121">予定なし。</span><span class="sxs-lookup"><span data-stu-id="bf1eb-121">The user is available.</span></span>  <br/> |
|<span data-ttu-id="bf1eb-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bf1eb-122">0x00000001</span></span>  <br/> |<span data-ttu-id="bf1eb-123">ユーザーに予定されている予定のイベントがあります。</span><span class="sxs-lookup"><span data-stu-id="bf1eb-123">The user has a tentative event scheduled.</span></span>  <br/> |
|<span data-ttu-id="bf1eb-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="bf1eb-124">0x00000002</span></span>  <br/> |<span data-ttu-id="bf1eb-125">予定あり。</span><span class="sxs-lookup"><span data-stu-id="bf1eb-125">The user is busy.</span></span>  <br/> |
|<span data-ttu-id="bf1eb-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="bf1eb-126">0x00000003</span></span>  <br/> |<span data-ttu-id="bf1eb-127">外出中。</span><span class="sxs-lookup"><span data-stu-id="bf1eb-127">The user is out of office.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bf1eb-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bf1eb-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bf1eb-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bf1eb-129">Protocol specifications</span></span>

<span data-ttu-id="bf1eb-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf1eb-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf1eb-131">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="bf1eb-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bf1eb-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf1eb-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf1eb-133">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bf1eb-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bf1eb-134">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bf1eb-134">Header files</span></span>

<span data-ttu-id="bf1eb-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf1eb-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf1eb-136">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bf1eb-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf1eb-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf1eb-137">See also</span></span>



[<span data-ttu-id="bf1eb-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bf1eb-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf1eb-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bf1eb-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf1eb-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bf1eb-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf1eb-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bf1eb-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

