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
ms.openlocfilehash: 7ad68a8ba527879871e79dd85e79d577291d32a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335442"
---
# <a name="pidtagownerappointmentid-canonical-property"></a><span data-ttu-id="8a567-103">PidTagOwnerAppointmentId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8a567-103">PidTagOwnerAppointmentId Canonical Property</span></span>

  
  
<span data-ttu-id="8a567-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a567-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a567-105">所有者のスケジュールにある予定の識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8a567-105">Contains an identifier for an appointment in the owner's schedule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a567-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8a567-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a567-107">PR_OWNER_APPT_ID</span><span class="sxs-lookup"><span data-stu-id="8a567-107">PR_OWNER_APPT_ID</span></span>  <br/> |
|<span data-ttu-id="8a567-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8a567-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a567-109">0x0062</span><span class="sxs-lookup"><span data-stu-id="8a567-109">0x0062</span></span>  <br/> |
|<span data-ttu-id="8a567-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8a567-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a567-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8a567-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8a567-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8a567-112">Area:</span></span>  <br/> |<span data-ttu-id="8a567-113">予定</span><span class="sxs-lookup"><span data-stu-id="8a567-113">Appointment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a567-114">解説</span><span class="sxs-lookup"><span data-stu-id="8a567-114">Remarks</span></span>

<span data-ttu-id="8a567-115">このプロパティは、会議出席依頼で使用されます。</span><span class="sxs-lookup"><span data-stu-id="8a567-115">This property is used in meeting requests.</span></span> <span data-ttu-id="8a567-116">これはエントリ識別子を表すものではなく、送信者のスケジュール内の予定を一意に識別する長整数型 (long) です。</span><span class="sxs-lookup"><span data-stu-id="8a567-116">It does not represent an entry identifier, but a long integer that uniquely identifies the appointment within the sender's schedule.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8a567-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8a567-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8a567-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8a567-118">Protocol specifications</span></span>

<span data-ttu-id="8a567-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a567-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a567-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8a567-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8a567-121">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a567-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a567-122">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a567-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="8a567-123">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a567-123">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a567-124">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="8a567-124">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8a567-125">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a567-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a567-126">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="8a567-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8a567-127">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="8a567-127">Header files</span></span>

<span data-ttu-id="8a567-128">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a567-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a567-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8a567-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a567-130">mapitags</span><span class="sxs-lookup"><span data-stu-id="8a567-130">mapitags.h</span></span>
  
> <span data-ttu-id="8a567-131">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8a567-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a567-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="8a567-132">See also</span></span>



[<span data-ttu-id="8a567-133">PidTagOriginalAuthorSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8a567-133">PidTagOriginalAuthorSearchKey Canonical Property</span></span>](pidtagoriginalauthorsearchkey-canonical-property.md)


[<span data-ttu-id="8a567-134">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8a567-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a567-135">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8a567-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a567-136">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8a567-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a567-137">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8a567-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

