---
title: PidLidToAttendeesString 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToAttendeesString
api_type:
- COM
ms.assetid: ca1eedba-c617-4403-8490-315ab75f2edb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ea0cd256b025ae519272f32522bebbe6e9e17b5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339815"
---
# <a name="pidlidtoattendeesstring-canonical-property"></a><span data-ttu-id="3fa53-103">PidLidToAttendeesString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3fa53-103">PidLidToAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="3fa53-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fa53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fa53-105">必須の出席者であるすべての送信可能な出席者の一覧が含まれる。</span><span class="sxs-lookup"><span data-stu-id="3fa53-105">Contains a list of all the sendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3fa53-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3fa53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3fa53-107">dispidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="3fa53-107">dispidToAttendeesString</span></span>  <br/> |
|<span data-ttu-id="3fa53-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="3fa53-108">Property set:</span></span>  <br/> |<span data-ttu-id="3fa53-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="3fa53-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="3fa53-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="3fa53-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3fa53-111">0x0000823B</span><span class="sxs-lookup"><span data-stu-id="3fa53-111">0x0000823B</span></span>  <br/> |
|<span data-ttu-id="3fa53-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3fa53-112">Data type:</span></span>  <br/> |<span data-ttu-id="3fa53-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3fa53-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3fa53-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="3fa53-114">Area:</span></span>  <br/> |<span data-ttu-id="3fa53-115">会議</span><span class="sxs-lookup"><span data-stu-id="3fa53-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fa53-116">注釈</span><span class="sxs-lookup"><span data-stu-id="3fa53-116">Remarks</span></span>

<span data-ttu-id="3fa53-117">各出席者の値は、PR_DISPLAY_NAME **の** アドレス帳のプロパティ ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) です。</span><span class="sxs-lookup"><span data-stu-id="3fa53-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="3fa53-118">個別のエントリは、セミコロンで区切り、その後にスペースを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fa53-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="3fa53-119">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="3fa53-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3fa53-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3fa53-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3fa53-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3fa53-121">Protocol specifications</span></span>

<span data-ttu-id="3fa53-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fa53-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fa53-123">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="3fa53-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3fa53-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fa53-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fa53-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3fa53-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3fa53-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3fa53-126">Header files</span></span>

<span data-ttu-id="3fa53-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3fa53-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="3fa53-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3fa53-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3fa53-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="3fa53-129">See also</span></span>



[<span data-ttu-id="3fa53-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3fa53-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3fa53-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3fa53-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3fa53-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3fa53-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3fa53-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3fa53-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

