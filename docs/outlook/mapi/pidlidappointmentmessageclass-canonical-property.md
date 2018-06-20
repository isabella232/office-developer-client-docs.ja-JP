---
title: PidLidAppointmentMessageClass の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentMessageClass
api_type:
- COM
ms.assetid: 8b8c8484-0cb4-4842-8b11-de42d97e0140
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8777b2119e6beefc4d69dc0babfc8672df3a468b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801730"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a><span data-ttu-id="9081d-103">PidLidAppointmentMessageClass の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="9081d-103">PidLidAppointmentMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="9081d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9081d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9081d-105">会議出席依頼から生成される会議の**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="9081d-105">Indicates the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the meeting that is to be generated from the meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9081d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="9081d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9081d-107">dispidApptMessageClass</span><span class="sxs-lookup"><span data-stu-id="9081d-107">dispidApptMessageClass</span></span>  <br/> |
|<span data-ttu-id="9081d-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="9081d-108">Property set:</span></span>  <br/> |<span data-ttu-id="9081d-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="9081d-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="9081d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9081d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9081d-111">0x00000024</span><span class="sxs-lookup"><span data-stu-id="9081d-111">0x00000024</span></span>  <br/> |
|<span data-ttu-id="9081d-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="9081d-112">Data type:</span></span>  <br/> |<span data-ttu-id="9081d-113">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="9081d-113">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="9081d-114">領域:</span><span class="sxs-lookup"><span data-stu-id="9081d-114">Area:</span></span>  <br/> |<span data-ttu-id="9081d-115">会議</span><span class="sxs-lookup"><span data-stu-id="9081d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9081d-116">備考</span><span class="sxs-lookup"><span data-stu-id="9081d-116">Remarks</span></span>

<span data-ttu-id="9081d-117">このプロパティの値は"IPM をする必要がありますか.予定""IPM に付けられますか.予定。"です。</span><span class="sxs-lookup"><span data-stu-id="9081d-117">The value of this property must either be "IPM.Appointment" or be prefixed with "IPM.Appointment.".</span></span> <span data-ttu-id="9081d-118">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="9081d-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9081d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9081d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9081d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9081d-120">Protocol specifications</span></span>

<span data-ttu-id="9081d-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9081d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9081d-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9081d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9081d-123">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9081d-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9081d-124">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9081d-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9081d-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9081d-125">Header files</span></span>

<span data-ttu-id="9081d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9081d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9081d-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9081d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9081d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9081d-128">See also</span></span>



[<span data-ttu-id="9081d-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9081d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9081d-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9081d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9081d-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="9081d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9081d-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="9081d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

