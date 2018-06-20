---
title: PidLidBusyStatus の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 926f0425a4a59cad4280917573c974375c94f50b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801833"
---
# <a name="pidlidbusystatus-canonical-property"></a><span data-ttu-id="0d8f8-103">PidLidBusyStatus の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="0d8f8-103">PidLidBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="0d8f8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d8f8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d8f8-105">予定の有無を表します。</span><span class="sxs-lookup"><span data-stu-id="0d8f8-105">Represents the user's availability for an appointment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d8f8-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="0d8f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d8f8-107">dispidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="0d8f8-107">dispidBusyStatus</span></span>  <br/> |
|<span data-ttu-id="0d8f8-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0d8f8-108">Property set:</span></span>  <br/> |<span data-ttu-id="0d8f8-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0d8f8-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0d8f8-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0d8f8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0d8f8-111">0x00008205</span><span class="sxs-lookup"><span data-stu-id="0d8f8-111">0x00008205</span></span>  <br/> |
|<span data-ttu-id="0d8f8-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="0d8f8-112">Data type:</span></span>  <br/> |<span data-ttu-id="0d8f8-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0d8f8-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0d8f8-114">領域:</span><span class="sxs-lookup"><span data-stu-id="0d8f8-114">Area:</span></span>  <br/> |<span data-ttu-id="0d8f8-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="0d8f8-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d8f8-116">備考</span><span class="sxs-lookup"><span data-stu-id="0d8f8-116">Remarks</span></span>

<span data-ttu-id="0d8f8-117">このプロパティは、オブジェクトが記載されているイベントで、ユーザーの可用性を指定し、以下に指定した値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d8f8-117">This property specifies the availability of a user for the event described by the object and must be one of the values specified below.</span></span>
  
|<span data-ttu-id="0d8f8-118">**値**</span><span class="sxs-lookup"><span data-stu-id="0d8f8-118">**Value**</span></span>|<span data-ttu-id="0d8f8-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="0d8f8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0d8f8-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d8f8-120">0x00000000</span></span>  <br/> |<span data-ttu-id="0d8f8-121">予定なし。</span><span class="sxs-lookup"><span data-stu-id="0d8f8-121">The user is available.</span></span>  <br/> |
|<span data-ttu-id="0d8f8-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0d8f8-122">0x00000001</span></span>  <br/> |<span data-ttu-id="0d8f8-123">ユーザーは、予定されている仮の予定のイベントです。</span><span class="sxs-lookup"><span data-stu-id="0d8f8-123">The user has a tentative event scheduled.</span></span>  <br/> |
|<span data-ttu-id="0d8f8-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0d8f8-124">0x00000002</span></span>  <br/> |<span data-ttu-id="0d8f8-125">予定あり。</span><span class="sxs-lookup"><span data-stu-id="0d8f8-125">The user is busy.</span></span>  <br/> |
|<span data-ttu-id="0d8f8-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="0d8f8-126">0x00000003</span></span>  <br/> |<span data-ttu-id="0d8f8-127">外出中。</span><span class="sxs-lookup"><span data-stu-id="0d8f8-127">The user is out of office.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0d8f8-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0d8f8-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0d8f8-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0d8f8-129">Protocol specifications</span></span>

<span data-ttu-id="0d8f8-130">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d8f8-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d8f8-131">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0d8f8-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0d8f8-132">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d8f8-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d8f8-133">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d8f8-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0d8f8-134">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0d8f8-134">Header files</span></span>

<span data-ttu-id="0d8f8-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d8f8-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d8f8-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0d8f8-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d8f8-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d8f8-137">See also</span></span>



[<span data-ttu-id="0d8f8-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0d8f8-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d8f8-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0d8f8-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d8f8-140">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="0d8f8-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d8f8-141">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="0d8f8-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

