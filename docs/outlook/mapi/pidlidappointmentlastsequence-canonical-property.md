---
title: PidLidAppointmentLastSequence の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentLastSequence
api_type:
- COM
ms.assetid: 52fa57be-746d-4b80-92b6-2ba83f796325
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 425bb54f63f6a87c2f1ae6bffef9ce2b042de6bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19801738"
---
# <a name="pidlidappointmentlastsequence-canonical-property"></a><span data-ttu-id="7d003-103">PidLidAppointmentLastSequence の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7d003-103">PidLidAppointmentLastSequence Canonical Property</span></span>

  
  
<span data-ttu-id="7d003-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d003-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d003-105">開催者、出席者に送信された最後のシーケンス番号を示します。</span><span class="sxs-lookup"><span data-stu-id="7d003-105">Indicates to the organizer the last sequence number that was sent to any attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d003-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7d003-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d003-107">dispidApptLastSequence</span><span class="sxs-lookup"><span data-stu-id="7d003-107">dispidApptLastSequence</span></span>  <br/> |
|<span data-ttu-id="7d003-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7d003-108">Property set:</span></span>  <br/> |<span data-ttu-id="7d003-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="7d003-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="7d003-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7d003-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7d003-111">0x00008203</span><span class="sxs-lookup"><span data-stu-id="7d003-111">0x00008203</span></span>  <br/> |
|<span data-ttu-id="7d003-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="7d003-112">Data type:</span></span>  <br/> |<span data-ttu-id="7d003-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7d003-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7d003-114">領域:</span><span class="sxs-lookup"><span data-stu-id="7d003-114">Area:</span></span>  <br/> |<span data-ttu-id="7d003-115">会議</span><span class="sxs-lookup"><span data-stu-id="7d003-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d003-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="7d003-116">Remarks</span></span>

<span data-ttu-id="7d003-117">このプロパティには、出席者の意味はありません。</span><span class="sxs-lookup"><span data-stu-id="7d003-117">This property has no meaning for an attendee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7d003-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7d003-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d003-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7d003-119">Protocol specifications</span></span>

<span data-ttu-id="7d003-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d003-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d003-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7d003-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7d003-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d003-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d003-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7d003-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d003-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7d003-124">Header files</span></span>

<span data-ttu-id="7d003-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d003-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d003-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7d003-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d003-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="7d003-127">See also</span></span>



[<span data-ttu-id="7d003-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7d003-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d003-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7d003-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d003-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7d003-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d003-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="7d003-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

