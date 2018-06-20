---
title: PidTagRecipientProposedStartTime の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedStartTime
api_type:
- COM
ms.assetid: 6687ff62-7ac6-409c-8c87-4e09d38e45f1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 65d5c2f94da219fc1cb87384ebdd3c1cf34bd9a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803287"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a><span data-ttu-id="6a68c-103">PidTagRecipientProposedStartTime の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6a68c-103">PidTagRecipientProposedStartTime Canonical Property</span></span>

  
  
<span data-ttu-id="6a68c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6a68c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6a68c-105">提案された会議の開始時刻を示します。</span><span class="sxs-lookup"><span data-stu-id="6a68c-105">Indicates a proposed starting time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a68c-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="6a68c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6a68c-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span><span class="sxs-lookup"><span data-stu-id="6a68c-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span></span>  <br/> |
|<span data-ttu-id="6a68c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6a68c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6a68c-109">0x5FE3</span><span class="sxs-lookup"><span data-stu-id="6a68c-109">0x5FE3</span></span>  <br/> |
|<span data-ttu-id="6a68c-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="6a68c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6a68c-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="6a68c-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="6a68c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6a68c-112">Area:</span></span>  <br/> |<span data-ttu-id="6a68c-113">トランスポートにおける受取人</span><span class="sxs-lookup"><span data-stu-id="6a68c-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a68c-114">備考</span><span class="sxs-lookup"><span data-stu-id="6a68c-114">Remarks</span></span>

<span data-ttu-id="6a68c-115">このプロパティの値が**dispidApptStartWhole** ([の値として設定するのには、出席者が要求した値を示す**PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) プロパティの値を設定すると、TRUE に設定するPidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) 会議オブジェクトのインスタンスを 1 つまたは例外オブジェクトのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="6a68c-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6a68c-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6a68c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6a68c-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6a68c-117">Protocol specifications</span></span>

<span data-ttu-id="6a68c-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a68c-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a68c-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6a68c-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6a68c-120">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a68c-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a68c-121">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6a68c-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6a68c-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6a68c-122">Header files</span></span>

<span data-ttu-id="6a68c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6a68c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a68c-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6a68c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6a68c-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6a68c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="6a68c-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6a68c-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a68c-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="6a68c-127">See also</span></span>



[<span data-ttu-id="6a68c-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6a68c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a68c-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6a68c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a68c-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="6a68c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a68c-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="6a68c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

