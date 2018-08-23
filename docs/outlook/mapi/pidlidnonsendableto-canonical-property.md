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
ms.openlocfilehash: e4875ff12d494b1d259c4647ff925243e55ee281
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586614"
---
# <a name="pidlidnonsendableto-canonical-property"></a><span data-ttu-id="b8374-103">PidLidNonSendableTo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8374-103">PidLidNonSendableTo Canonical Property</span></span>

  
  
<span data-ttu-id="b8374-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8374-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8374-105">すべての連絡先である出席者も必須出席者の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b8374-105">Contains a list of all the unsendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b8374-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b8374-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b8374-107">dispidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="b8374-107">dispidNonSendableTo</span></span>  <br/> |
|<span data-ttu-id="b8374-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b8374-108">Property set:</span></span>  <br/> |<span data-ttu-id="b8374-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b8374-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b8374-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b8374-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b8374-111">0x00008536</span><span class="sxs-lookup"><span data-stu-id="b8374-111">0x00008536</span></span>  <br/> |
|<span data-ttu-id="b8374-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b8374-112">Data type:</span></span>  <br/> |<span data-ttu-id="b8374-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b8374-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b8374-114">領域:</span><span class="sxs-lookup"><span data-stu-id="b8374-114">Area:</span></span>  <br/> |<span data-ttu-id="b8374-115">会議</span><span class="sxs-lookup"><span data-stu-id="b8374-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8374-116">注釈</span><span class="sxs-lookup"><span data-stu-id="b8374-116">Remarks</span></span>

<span data-ttu-id="b8374-117">各出席者の値は、出席者のアドレス帳の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="b8374-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="b8374-118">別のエントリは、スペースの後にセミコロンで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8374-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="b8374-119">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="b8374-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b8374-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b8374-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b8374-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b8374-121">Protocol specifications</span></span>

<span data-ttu-id="b8374-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8374-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8374-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b8374-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b8374-124">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8374-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8374-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b8374-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b8374-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b8374-126">Header files</span></span>

<span data-ttu-id="b8374-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b8374-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b8374-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b8374-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8374-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="b8374-129">See also</span></span>



[<span data-ttu-id="b8374-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8374-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b8374-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8374-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b8374-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b8374-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b8374-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b8374-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

