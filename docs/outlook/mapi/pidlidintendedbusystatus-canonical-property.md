---
title: PidLidIntendedBusyStatus の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIntendedBusyStatus
api_type:
- COM
ms.assetid: 84221dd3-de71-4c10-abd7-9f15aefd02ed
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 30f1e2389698f5ec96874f46a685a7e087dbb773
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802010"
---
# <a name="pidlidintendedbusystatus-canonical-property"></a><span data-ttu-id="523aa-103">PidLidIntendedBusyStatus の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="523aa-103">PidLidIntendedBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="523aa-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="523aa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="523aa-105">会議出席依頼または会議の更新が送信された場合は、開催者の予定表で会議の**dispidBusyStatus** ([PidLidBusyStatus](pidlidbusystatus-canonical-property.md)) プロパティの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="523aa-105">Specifies the value of the **dispidBusyStatus** ([PidLidBusyStatus](pidlidbusystatus-canonical-property.md)) property on the meeting in the organizer's calendar when the meeting request or meeting update was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="523aa-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="523aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="523aa-107">dispidIntendedBusyStatus</span><span class="sxs-lookup"><span data-stu-id="523aa-107">dispidIntendedBusyStatus</span></span>  <br/> |
|<span data-ttu-id="523aa-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="523aa-108">Property set:</span></span>  <br/> |<span data-ttu-id="523aa-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="523aa-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="523aa-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="523aa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="523aa-111">0x00008224</span><span class="sxs-lookup"><span data-stu-id="523aa-111">0x00008224</span></span>  <br/> |
|<span data-ttu-id="523aa-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="523aa-112">Data type:</span></span>  <br/> |<span data-ttu-id="523aa-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="523aa-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="523aa-114">領域:</span><span class="sxs-lookup"><span data-stu-id="523aa-114">Area:</span></span>  <br/> |<span data-ttu-id="523aa-115">会議</span><span class="sxs-lookup"><span data-stu-id="523aa-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="523aa-116">備考</span><span class="sxs-lookup"><span data-stu-id="523aa-116">Remarks</span></span>

<span data-ttu-id="523aa-117">このプロパティで使用できる値は、プロパティ**dispidBusyStatus**の場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="523aa-117">The allowable values of this property are the same as those for the property **dispidBusyStatus**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="523aa-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="523aa-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="523aa-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="523aa-119">Protocol specifications</span></span>

<span data-ttu-id="523aa-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="523aa-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="523aa-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="523aa-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="523aa-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="523aa-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="523aa-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="523aa-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="523aa-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="523aa-124">Header files</span></span>

<span data-ttu-id="523aa-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="523aa-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="523aa-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="523aa-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="523aa-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="523aa-127">See also</span></span>



[<span data-ttu-id="523aa-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="523aa-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="523aa-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="523aa-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="523aa-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="523aa-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="523aa-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="523aa-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

