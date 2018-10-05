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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391333"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="86b83-103">PidLidAppointmentStateFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="86b83-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="86b83-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86b83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86b83-105">オブジェクトの状態を示すビット フィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="86b83-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86b83-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="86b83-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86b83-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="86b83-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="86b83-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="86b83-108">Property set:</span></span>  <br/> |<span data-ttu-id="86b83-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="86b83-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="86b83-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="86b83-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="86b83-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="86b83-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="86b83-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="86b83-112">Data type:</span></span>  <br/> |<span data-ttu-id="86b83-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="86b83-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="86b83-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="86b83-114">Area:</span></span>  <br/> |<span data-ttu-id="86b83-115">会議</span><span class="sxs-lookup"><span data-stu-id="86b83-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86b83-116">備考</span><span class="sxs-lookup"><span data-stu-id="86b83-116">Remarks</span></span>

<span data-ttu-id="86b83-117">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="86b83-117">This property is not required.</span></span> <span data-ttu-id="86b83-118">以下は、個々 のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="86b83-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="86b83-119">M (asfMeeting、0x00000001)</span><span class="sxs-lookup"><span data-stu-id="86b83-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="86b83-120">このフラグは、オブジェクトが、会議オブジェクト、または会議に関連するオブジェクトであることを示します。</span><span class="sxs-lookup"><span data-stu-id="86b83-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="86b83-121">R (asfReceived、0x00000002)</span><span class="sxs-lookup"><span data-stu-id="86b83-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="86b83-122">このフラグは、表示されたオブジェクトが他のユーザーから受信されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="86b83-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="86b83-123">C (asfCanceled、0x00000004)</span><span class="sxs-lookup"><span data-stu-id="86b83-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="86b83-124">このフラグは、オブジェクトによって表される、会議オブジェクトがキャンセルされたことを示します。</span><span class="sxs-lookup"><span data-stu-id="86b83-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="86b83-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="86b83-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="86b83-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="86b83-126">Protocol specifications</span></span>

<span data-ttu-id="86b83-127">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86b83-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86b83-128">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="86b83-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="86b83-129">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86b83-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86b83-130">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="86b83-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="86b83-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="86b83-131">Header files</span></span>

<span data-ttu-id="86b83-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86b83-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="86b83-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="86b83-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86b83-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="86b83-134">See also</span></span>



[<span data-ttu-id="86b83-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="86b83-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86b83-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="86b83-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86b83-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="86b83-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86b83-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="86b83-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

