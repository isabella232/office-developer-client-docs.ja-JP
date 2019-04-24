---
title: PidLidCcAttendeesString 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCcAttendeesString
api_type:
- COM
ms.assetid: 697d5c93-ec7f-4608-9866-9e249a093dbc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 12cdbfcc140fb5ea3bb15a2db93f3689923d9390
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344969"
---
# <a name="pidlidccattendeesstring-canonical-property"></a><span data-ttu-id="92f31-103">PidLidCcAttendeesString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="92f31-103">PidLidCcAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="92f31-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92f31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92f31-105">任意出席者でもあるすべての送信可能の出席者の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="92f31-105">Contains a list of all the sendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92f31-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="92f31-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92f31-107">dispidCCAttendeesString</span><span class="sxs-lookup"><span data-stu-id="92f31-107">dispidCCAttendeesString</span></span>  <br/> |
|<span data-ttu-id="92f31-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="92f31-108">Property set:</span></span>  <br/> |<span data-ttu-id="92f31-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="92f31-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="92f31-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="92f31-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="92f31-111">0x0000823c</span><span class="sxs-lookup"><span data-stu-id="92f31-111">0x0000823C</span></span>  <br/> |
|<span data-ttu-id="92f31-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="92f31-112">Data type:</span></span>  <br/> |<span data-ttu-id="92f31-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="92f31-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="92f31-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="92f31-114">Area:</span></span>  <br/> |<span data-ttu-id="92f31-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="92f31-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92f31-116">解説</span><span class="sxs-lookup"><span data-stu-id="92f31-116">Remarks</span></span>

<span data-ttu-id="92f31-117">各出席者の値は、出席者のアドレス帳の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="92f31-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's address book.</span></span> <span data-ttu-id="92f31-118">エントリを区切るには、セミコロンの後にスペースを付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="92f31-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="92f31-119">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="92f31-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="92f31-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="92f31-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="92f31-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="92f31-121">Protocol specifications</span></span>

<span data-ttu-id="92f31-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92f31-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92f31-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="92f31-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="92f31-124">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92f31-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92f31-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="92f31-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="92f31-126">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92f31-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92f31-127">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="92f31-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="92f31-128">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="92f31-128">Header files</span></span>

<span data-ttu-id="92f31-129">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92f31-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="92f31-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="92f31-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92f31-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="92f31-131">See also</span></span>



[<span data-ttu-id="92f31-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="92f31-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92f31-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="92f31-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92f31-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="92f31-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92f31-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="92f31-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

