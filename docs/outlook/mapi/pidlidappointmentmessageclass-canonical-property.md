---
title: PidLidAppointmentMessageClass 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8777b2119e6beefc4d69dc0babfc8672df3a468b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801730"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a><span data-ttu-id="5ec21-103">PidLidAppointmentMessageClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5ec21-103">PidLidAppointmentMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="5ec21-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5ec21-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5ec21-105">会議出席依頼から生成される会議の**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="5ec21-105">Indicates the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the meeting that is to be generated from the meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ec21-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5ec21-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ec21-107">dispidApptMessageClass</span><span class="sxs-lookup"><span data-stu-id="5ec21-107">dispidApptMessageClass</span></span>  <br/> |
|<span data-ttu-id="5ec21-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec21-108">Property set:</span></span>  <br/> |<span data-ttu-id="5ec21-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="5ec21-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="5ec21-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5ec21-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5ec21-111">0x00000024</span><span class="sxs-lookup"><span data-stu-id="5ec21-111">0x00000024</span></span>  <br/> |
|<span data-ttu-id="5ec21-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5ec21-112">Data type:</span></span>  <br/> |<span data-ttu-id="5ec21-113">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="5ec21-113">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="5ec21-114">領域:</span><span class="sxs-lookup"><span data-stu-id="5ec21-114">Area:</span></span>  <br/> |<span data-ttu-id="5ec21-115">会議</span><span class="sxs-lookup"><span data-stu-id="5ec21-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ec21-116">注釈</span><span class="sxs-lookup"><span data-stu-id="5ec21-116">Remarks</span></span>

<span data-ttu-id="5ec21-117">このプロパティの値は"IPM をする必要がありますか.予定""IPM に付けられますか.予定。"です。</span><span class="sxs-lookup"><span data-stu-id="5ec21-117">The value of this property must either be "IPM.Appointment" or be prefixed with "IPM.Appointment.".</span></span> <span data-ttu-id="5ec21-118">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="5ec21-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5ec21-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5ec21-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5ec21-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5ec21-120">Protocol specifications</span></span>

<span data-ttu-id="5ec21-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ec21-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ec21-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5ec21-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5ec21-123">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ec21-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ec21-124">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ec21-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5ec21-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5ec21-125">Header files</span></span>

<span data-ttu-id="5ec21-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ec21-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ec21-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5ec21-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ec21-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ec21-128">See also</span></span>



[<span data-ttu-id="5ec21-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5ec21-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ec21-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5ec21-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ec21-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5ec21-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ec21-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5ec21-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

