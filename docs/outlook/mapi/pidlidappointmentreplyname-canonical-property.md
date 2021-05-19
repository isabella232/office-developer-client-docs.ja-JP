---
title: PidLidAppointmentReplyName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyName
api_type:
- COM
ms.assetid: 2f3a44d1-600f-412e-bc89-078841db5308
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f6707c49c70804aeb757119aa411ca4059e378eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356043"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a><span data-ttu-id="c4351-103">PidLidAppointmentReplyName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4351-103">PidLidAppointmentReplyName Canonical Property</span></span>

  
  
<span data-ttu-id="c4351-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4351-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4351-105">会議出席依頼または会議の更新オブジェクトに最後に返信したユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="c4351-105">Specifies the user who last replied to the meeting request or meeting update object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4351-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c4351-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4351-107">dispidApptReplyName</span><span class="sxs-lookup"><span data-stu-id="c4351-107">dispidApptReplyName</span></span>  <br/> |
|<span data-ttu-id="c4351-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="c4351-108">Property set:</span></span>  <br/> |<span data-ttu-id="c4351-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="c4351-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="c4351-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c4351-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c4351-111">0x00008230</span><span class="sxs-lookup"><span data-stu-id="c4351-111">0x00008230</span></span>  <br/> |
|<span data-ttu-id="c4351-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c4351-112">Data type:</span></span>  <br/> |<span data-ttu-id="c4351-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c4351-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c4351-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="c4351-114">Area:</span></span>  <br/> |<span data-ttu-id="c4351-115">会議</span><span class="sxs-lookup"><span data-stu-id="c4351-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4351-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c4351-116">Remarks</span></span>

<span data-ttu-id="c4351-117">このプロパティは、代理人が応答した場合にのみ委任者に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="c4351-117">This property is only set for a delegator when a delegate responded.</span></span> <span data-ttu-id="c4351-118">値は、代理人の **ストアPR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) プロパティと等しくなります。</span><span class="sxs-lookup"><span data-stu-id="c4351-118">The value is equal to the **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) property for the delegate's store.</span></span> <span data-ttu-id="c4351-119">このプロパティは、開催者には意味はありません。</span><span class="sxs-lookup"><span data-stu-id="c4351-119">This property has no meaning for the organizer.</span></span> <span data-ttu-id="c4351-120">詳細については **、「PR_MAILBOX_OWNER_NAME** [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)で指定されているストア オブジェクト プロトコル」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4351-120">For details on **PR_MAILBOX_OWNER_NAME**, see store object protocol specified in [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c4351-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c4351-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4351-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c4351-122">Protocol specifications</span></span>

<span data-ttu-id="c4351-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4351-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4351-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c4351-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c4351-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4351-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4351-126">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="c4351-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c4351-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4351-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4351-128">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4351-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4351-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c4351-129">Header files</span></span>

<span data-ttu-id="c4351-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4351-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4351-131">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c4351-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4351-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="c4351-132">See also</span></span>



[<span data-ttu-id="c4351-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c4351-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4351-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4351-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4351-135">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c4351-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4351-136">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c4351-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

