---
title: PidLidAppointmentStateFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStateFlags
api_type:
- COM
ms.assetid: 1e5f0f83-c40b-4b3a-8492-61d1b53b1e3c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e365c78ea6457e7da79e3d1c749baa922a01acbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345361"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="87f14-103">PidLidAppointmentStateFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="87f14-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="87f14-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87f14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87f14-105">オブジェクトの状態を示すビットフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="87f14-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87f14-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="87f14-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87f14-107">dispidapptstateflags</span><span class="sxs-lookup"><span data-stu-id="87f14-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="87f14-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="87f14-108">Property set:</span></span>  <br/> |<span data-ttu-id="87f14-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="87f14-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="87f14-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="87f14-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="87f14-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="87f14-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="87f14-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="87f14-112">Data type:</span></span>  <br/> |<span data-ttu-id="87f14-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="87f14-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="87f14-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="87f14-114">Area:</span></span>  <br/> |<span data-ttu-id="87f14-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="87f14-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87f14-116">解説</span><span class="sxs-lookup"><span data-stu-id="87f14-116">Remarks</span></span>

<span data-ttu-id="87f14-117">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="87f14-117">This property is not required.</span></span> <span data-ttu-id="87f14-118">設定できる個別のフラグを次に示します。</span><span class="sxs-lookup"><span data-stu-id="87f14-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="87f14-119">M (asfmeeting、0x00000001)</span><span class="sxs-lookup"><span data-stu-id="87f14-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="87f14-120">このフラグは、オブジェクトが会議オブジェクトまたは会議関連オブジェクトであることを示します。</span><span class="sxs-lookup"><span data-stu-id="87f14-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="87f14-121">R (asfreceived, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="87f14-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="87f14-122">このフラグは、表示されたオブジェクトが他のユーザーから受信したものであることを示します。</span><span class="sxs-lookup"><span data-stu-id="87f14-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="87f14-123">C (asfcanceled, 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="87f14-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="87f14-124">このフラグは、オブジェクトによって表される会議オブジェクトがキャンセルされたことを示します。</span><span class="sxs-lookup"><span data-stu-id="87f14-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="87f14-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="87f14-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87f14-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="87f14-126">Protocol specifications</span></span>

<span data-ttu-id="87f14-127">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87f14-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87f14-128">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="87f14-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="87f14-129">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87f14-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87f14-130">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="87f14-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87f14-131">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="87f14-131">Header files</span></span>

<span data-ttu-id="87f14-132">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87f14-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="87f14-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="87f14-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87f14-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="87f14-134">See also</span></span>



[<span data-ttu-id="87f14-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="87f14-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87f14-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="87f14-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87f14-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="87f14-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87f14-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="87f14-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

