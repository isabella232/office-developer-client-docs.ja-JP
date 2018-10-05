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
ms.openlocfilehash: 7b7cfe1fc1068e5b5b228c4de4c9317d9bcbbc66
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401007"
---
# <a name="pidlidnonsendablebcc-canonical-property"></a><span data-ttu-id="bb475-103">PidLidNonSendableBcc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb475-103">PidLidNonSendableBcc Canonical Property</span></span>

  
  
<span data-ttu-id="bb475-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb475-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb475-105">リソースである連絡先すべての出席者の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bb475-105">Contains a list of all the unsendable attendees who are resources.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb475-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bb475-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb475-107">dispidNonSendableBCC</span><span class="sxs-lookup"><span data-stu-id="bb475-107">dispidNonSendableBCC</span></span>  <br/> |
|<span data-ttu-id="bb475-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="bb475-108">Property set:</span></span>  <br/> |<span data-ttu-id="bb475-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="bb475-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="bb475-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bb475-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bb475-111">0x00008538</span><span class="sxs-lookup"><span data-stu-id="bb475-111">0x00008538</span></span>  <br/> |
|<span data-ttu-id="bb475-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bb475-112">Data type:</span></span>  <br/> |<span data-ttu-id="bb475-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bb475-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bb475-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="bb475-114">Area:</span></span>  <br/> |<span data-ttu-id="bb475-115">会議</span><span class="sxs-lookup"><span data-stu-id="bb475-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb475-116">備考</span><span class="sxs-lookup"><span data-stu-id="bb475-116">Remarks</span></span>

<span data-ttu-id="bb475-117">各出席者の値は、出席者のアドレス帳の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="bb475-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="bb475-118">別のエントリは、スペースの後にセミコロンで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb475-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="bb475-119">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="bb475-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bb475-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bb475-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb475-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bb475-121">Protocol specifications</span></span>

<span data-ttu-id="bb475-122">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb475-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb475-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="bb475-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb475-124">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb475-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb475-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb475-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="bb475-126">[[MS OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb475-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb475-127">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="bb475-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb475-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bb475-128">Header files</span></span>

<span data-ttu-id="bb475-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb475-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb475-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bb475-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb475-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb475-131">See also</span></span>



[<span data-ttu-id="bb475-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb475-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb475-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb475-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb475-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bb475-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb475-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bb475-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

