---
title: PidLidNonSendableTo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableTo
api_type:
- COM
ms.assetid: 90e14969-652b-422a-9b0a-ee99e58bc8d5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cc510cb9a4a79f977cb6c9721921833441df23c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394092"
---
# <a name="pidlidnonsendableto-canonical-property"></a><span data-ttu-id="e645d-103">PidLidNonSendableTo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e645d-103">PidLidNonSendableTo Canonical Property</span></span>

  
  
<span data-ttu-id="e645d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e645d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e645d-105">すべての連絡先である出席者も必須出席者の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e645d-105">Contains a list of all the unsendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e645d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e645d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e645d-107">dispidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="e645d-107">dispidNonSendableTo</span></span>  <br/> |
|<span data-ttu-id="e645d-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e645d-108">Property set:</span></span>  <br/> |<span data-ttu-id="e645d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e645d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e645d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e645d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e645d-111">0x00008536</span><span class="sxs-lookup"><span data-stu-id="e645d-111">0x00008536</span></span>  <br/> |
|<span data-ttu-id="e645d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e645d-112">Data type:</span></span>  <br/> |<span data-ttu-id="e645d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e645d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e645d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="e645d-114">Area:</span></span>  <br/> |<span data-ttu-id="e645d-115">会議</span><span class="sxs-lookup"><span data-stu-id="e645d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e645d-116">備考</span><span class="sxs-lookup"><span data-stu-id="e645d-116">Remarks</span></span>

<span data-ttu-id="e645d-117">各出席者の値は、出席者のアドレス帳の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="e645d-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="e645d-118">別のエントリは、スペースの後にセミコロンで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="e645d-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="e645d-119">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="e645d-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e645d-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e645d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e645d-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e645d-121">Protocol specifications</span></span>

<span data-ttu-id="e645d-122">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e645d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e645d-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e645d-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e645d-124">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e645d-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e645d-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e645d-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e645d-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e645d-126">Header files</span></span>

<span data-ttu-id="e645d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e645d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e645d-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e645d-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e645d-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e645d-129">See also</span></span>



[<span data-ttu-id="e645d-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e645d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e645d-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e645d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e645d-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e645d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e645d-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e645d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

