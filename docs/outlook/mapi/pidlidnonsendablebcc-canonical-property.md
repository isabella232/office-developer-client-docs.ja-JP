---
title: PidLidNonSendableBcc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBcc
api_type:
- COM
ms.assetid: c7523896-c391-443d-bd4e-cc13f3367f08
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c732bb1f4f8b973e1b267ca241c62c71254adcb1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563997"
---
# <a name="pidlidnonsendablebcc-canonical-property"></a><span data-ttu-id="2ec5d-103">PidLidNonSendableBcc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ec5d-103">PidLidNonSendableBcc Canonical Property</span></span>

  
  
<span data-ttu-id="2ec5d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ec5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ec5d-105">リソースである連絡先すべての出席者の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2ec5d-105">Contains a list of all the unsendable attendees who are resources.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ec5d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2ec5d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ec5d-107">dispidNonSendableBCC</span><span class="sxs-lookup"><span data-stu-id="2ec5d-107">dispidNonSendableBCC</span></span>  <br/> |
|<span data-ttu-id="2ec5d-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2ec5d-108">Property set:</span></span>  <br/> |<span data-ttu-id="2ec5d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="2ec5d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="2ec5d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="2ec5d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2ec5d-111">0x00008538</span><span class="sxs-lookup"><span data-stu-id="2ec5d-111">0x00008538</span></span>  <br/> |
|<span data-ttu-id="2ec5d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2ec5d-112">Data type:</span></span>  <br/> |<span data-ttu-id="2ec5d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2ec5d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2ec5d-114">領域:</span><span class="sxs-lookup"><span data-stu-id="2ec5d-114">Area:</span></span>  <br/> |<span data-ttu-id="2ec5d-115">会議</span><span class="sxs-lookup"><span data-stu-id="2ec5d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ec5d-116">注釈</span><span class="sxs-lookup"><span data-stu-id="2ec5d-116">Remarks</span></span>

<span data-ttu-id="2ec5d-117">各出席者の値は、出席者のアドレス帳の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="2ec5d-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="2ec5d-118">別のエントリは、スペースの後にセミコロンで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ec5d-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="2ec5d-119">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="2ec5d-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ec5d-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2ec5d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ec5d-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2ec5d-121">Protocol specifications</span></span>

<span data-ttu-id="2ec5d-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ec5d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ec5d-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ec5d-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2ec5d-124">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ec5d-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ec5d-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ec5d-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="2ec5d-126">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ec5d-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ec5d-127">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="2ec5d-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ec5d-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2ec5d-128">Header files</span></span>

<span data-ttu-id="2ec5d-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ec5d-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ec5d-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ec5d-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ec5d-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ec5d-131">See also</span></span>



[<span data-ttu-id="2ec5d-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ec5d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ec5d-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ec5d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ec5d-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2ec5d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ec5d-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2ec5d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

