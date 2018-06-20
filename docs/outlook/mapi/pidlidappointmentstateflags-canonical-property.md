---
title: PidLidAppointmentStateFlags の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 293eb489a1e926f0e60e823a536dacf6f409e353
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801805"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="1635a-103">PidLidAppointmentStateFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="1635a-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="1635a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1635a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1635a-105">オブジェクトの状態を示すビット フィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="1635a-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1635a-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="1635a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1635a-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="1635a-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="1635a-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="1635a-108">Property set:</span></span>  <br/> |<span data-ttu-id="1635a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="1635a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="1635a-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1635a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1635a-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="1635a-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="1635a-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="1635a-112">Data type:</span></span>  <br/> |<span data-ttu-id="1635a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1635a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1635a-114">領域:</span><span class="sxs-lookup"><span data-stu-id="1635a-114">Area:</span></span>  <br/> |<span data-ttu-id="1635a-115">会議</span><span class="sxs-lookup"><span data-stu-id="1635a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1635a-116">備考</span><span class="sxs-lookup"><span data-stu-id="1635a-116">Remarks</span></span>

<span data-ttu-id="1635a-117">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="1635a-117">This property is not required.</span></span> <span data-ttu-id="1635a-118">以下は、個々 のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1635a-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="1635a-119">M (asfMeeting、0x00000001)</span><span class="sxs-lookup"><span data-stu-id="1635a-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="1635a-120">このフラグは、オブジェクトが、会議オブジェクト、または会議に関連するオブジェクトであることを示します。</span><span class="sxs-lookup"><span data-stu-id="1635a-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="1635a-121">R (asfReceived、0x00000002)</span><span class="sxs-lookup"><span data-stu-id="1635a-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="1635a-122">このフラグは、表示されたオブジェクトが他のユーザーから受信されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="1635a-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="1635a-123">C (asfCanceled、0x00000004)</span><span class="sxs-lookup"><span data-stu-id="1635a-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="1635a-124">このフラグは、オブジェクトによって表される、会議オブジェクトがキャンセルされたことを示します。</span><span class="sxs-lookup"><span data-stu-id="1635a-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="1635a-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1635a-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1635a-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1635a-126">Protocol specifications</span></span>

<span data-ttu-id="1635a-127">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1635a-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1635a-128">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1635a-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1635a-129">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1635a-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1635a-130">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1635a-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1635a-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1635a-131">Header files</span></span>

<span data-ttu-id="1635a-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1635a-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="1635a-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1635a-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1635a-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="1635a-134">See also</span></span>



[<span data-ttu-id="1635a-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1635a-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1635a-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1635a-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1635a-137">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="1635a-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1635a-138">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="1635a-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

