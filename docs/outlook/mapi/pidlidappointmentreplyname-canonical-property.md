---
title: PidLidAppointmentReplyName の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5b6d88b60f9f5c6a01a92ecc5905f711fbf3ab3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801775"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a><span data-ttu-id="f15ca-103">PidLidAppointmentReplyName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f15ca-103">PidLidAppointmentReplyName Canonical Property</span></span>

  
  
<span data-ttu-id="f15ca-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f15ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f15ca-105">最後に会議出席依頼に返信したユーザーを指定するか、会議オブジェクトを更新します。</span><span class="sxs-lookup"><span data-stu-id="f15ca-105">Specifies the user who last replied to the meeting request or meeting update object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f15ca-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f15ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f15ca-107">dispidApptReplyName</span><span class="sxs-lookup"><span data-stu-id="f15ca-107">dispidApptReplyName</span></span>  <br/> |
|<span data-ttu-id="f15ca-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f15ca-108">Property set:</span></span>  <br/> |<span data-ttu-id="f15ca-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="f15ca-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="f15ca-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f15ca-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f15ca-111">0x00008230</span><span class="sxs-lookup"><span data-stu-id="f15ca-111">0x00008230</span></span>  <br/> |
|<span data-ttu-id="f15ca-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="f15ca-112">Data type:</span></span>  <br/> |<span data-ttu-id="f15ca-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f15ca-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f15ca-114">領域:</span><span class="sxs-lookup"><span data-stu-id="f15ca-114">Area:</span></span>  <br/> |<span data-ttu-id="f15ca-115">会議</span><span class="sxs-lookup"><span data-stu-id="f15ca-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f15ca-116">備考</span><span class="sxs-lookup"><span data-stu-id="f15ca-116">Remarks</span></span>

<span data-ttu-id="f15ca-117">代理人が反応したとき、このプロパティを代理人の設定のみ。</span><span class="sxs-lookup"><span data-stu-id="f15ca-117">This property is only set for a delegator when a delegate responded.</span></span> <span data-ttu-id="f15ca-118">値は**PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) は、代理人のストアになります。</span><span class="sxs-lookup"><span data-stu-id="f15ca-118">The value is equal to the **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) property for the delegate's store.</span></span> <span data-ttu-id="f15ca-119">このプロパティには、開催者の意味がありません。</span><span class="sxs-lookup"><span data-stu-id="f15ca-119">This property has no meaning for the organizer.</span></span> <span data-ttu-id="f15ca-120">**PR_MAILBOX_OWNER_NAME**の詳細については、「 [[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)で指定されたオブジェクト プロトコルを格納します。</span><span class="sxs-lookup"><span data-stu-id="f15ca-120">For details on **PR_MAILBOX_OWNER_NAME**, see store object protocol specified in [[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f15ca-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f15ca-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f15ca-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f15ca-122">Protocol specifications</span></span>

<span data-ttu-id="f15ca-123">[[MS OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f15ca-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f15ca-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f15ca-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f15ca-125">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f15ca-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f15ca-126">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f15ca-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f15ca-127">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f15ca-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f15ca-128">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f15ca-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f15ca-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f15ca-129">Header files</span></span>

<span data-ttu-id="f15ca-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f15ca-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="f15ca-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f15ca-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f15ca-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="f15ca-132">See also</span></span>



[<span data-ttu-id="f15ca-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f15ca-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f15ca-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f15ca-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f15ca-135">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="f15ca-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f15ca-136">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="f15ca-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

