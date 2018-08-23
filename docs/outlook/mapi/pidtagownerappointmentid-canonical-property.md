---
title: PidTagOwnerAppointmentId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnerAppointmentId
api_type:
- COM
ms.assetid: b5eea554-6bca-42d1-b943-1327f0d70584
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a6fc194a3ef7d82be656a8d6c3f5fb9ad8326ceb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803137"
---
# <a name="pidtagownerappointmentid-canonical-property"></a><span data-ttu-id="4a926-103">PidTagOwnerAppointmentId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a926-103">PidTagOwnerAppointmentId Canonical Property</span></span>

  
  
<span data-ttu-id="4a926-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a926-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a926-105">所有者のスケジュールで予定の識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4a926-105">Contains an identifier for an appointment in the owner's schedule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a926-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4a926-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a926-107">PR_OWNER_APPT_ID</span><span class="sxs-lookup"><span data-stu-id="4a926-107">PR_OWNER_APPT_ID</span></span>  <br/> |
|<span data-ttu-id="4a926-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4a926-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a926-109">0x0062</span><span class="sxs-lookup"><span data-stu-id="4a926-109">0x0062</span></span>  <br/> |
|<span data-ttu-id="4a926-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4a926-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a926-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4a926-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4a926-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4a926-112">Area:</span></span>  <br/> |<span data-ttu-id="4a926-113">Appointment</span><span class="sxs-lookup"><span data-stu-id="4a926-113">Appointment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a926-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4a926-114">Remarks</span></span>

<span data-ttu-id="4a926-115">このプロパティは、会議出席依頼で使用されます。</span><span class="sxs-lookup"><span data-stu-id="4a926-115">This property is used in meeting requests.</span></span> <span data-ttu-id="4a926-116">エントリの識別子ですが、送信者のスケジュールで予定を一意に識別する長整数型を表していません。</span><span class="sxs-lookup"><span data-stu-id="4a926-116">It does not represent an entry identifier, but a long integer that uniquely identifies the appointment within the sender's schedule.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4a926-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4a926-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a926-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4a926-118">Protocol specifications</span></span>

<span data-ttu-id="4a926-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a926-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a926-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4a926-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a926-121">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a926-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a926-122">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a926-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="4a926-123">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a926-123">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a926-124">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="4a926-124">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="4a926-125">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a926-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a926-126">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="4a926-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a926-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4a926-127">Header files</span></span>

<span data-ttu-id="4a926-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a926-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a926-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4a926-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a926-130">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4a926-130">mapitags.h</span></span>
  
> <span data-ttu-id="4a926-131">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4a926-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a926-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="4a926-132">See also</span></span>



[<span data-ttu-id="4a926-133">PidTagOriginalAuthorSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a926-133">PidTagOriginalAuthorSearchKey Canonical Property</span></span>](pidtagoriginalauthorsearchkey-canonical-property.md)


[<span data-ttu-id="4a926-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a926-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a926-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a926-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a926-136">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4a926-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a926-137">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4a926-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

