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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cc510cb9a4a79f977cb6c9721921833441df23c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345518"
---
# <a name="pidlidnonsendableto-canonical-property"></a><span data-ttu-id="59469-103">PidLidNonSendableTo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="59469-103">PidLidNonSendableTo Canonical Property</span></span>

  
  
<span data-ttu-id="59469-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59469-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59469-105">必須の出席者である、すべての送信不可の出席者の一覧が含まれる。</span><span class="sxs-lookup"><span data-stu-id="59469-105">Contains a list of all the unsendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59469-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="59469-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59469-107">dispidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="59469-107">dispidNonSendableTo</span></span>  <br/> |
|<span data-ttu-id="59469-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="59469-108">Property set:</span></span>  <br/> |<span data-ttu-id="59469-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="59469-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="59469-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="59469-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="59469-111">0x00008536</span><span class="sxs-lookup"><span data-stu-id="59469-111">0x00008536</span></span>  <br/> |
|<span data-ttu-id="59469-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="59469-112">Data type:</span></span>  <br/> |<span data-ttu-id="59469-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="59469-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="59469-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="59469-114">Area:</span></span>  <br/> |<span data-ttu-id="59469-115">会議</span><span class="sxs-lookup"><span data-stu-id="59469-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59469-116">注釈</span><span class="sxs-lookup"><span data-stu-id="59469-116">Remarks</span></span>

<span data-ttu-id="59469-117">各出席者の値は、PR_DISPLAY_NAME **の** アドレス帳のプロパティ ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) です。</span><span class="sxs-lookup"><span data-stu-id="59469-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="59469-118">個別のエントリは、セミコロンで区切り、その後にスペースを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59469-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="59469-119">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="59469-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="59469-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="59469-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="59469-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="59469-121">Protocol specifications</span></span>

<span data-ttu-id="59469-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59469-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59469-123">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="59469-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="59469-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59469-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59469-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="59469-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="59469-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="59469-126">Header files</span></span>

<span data-ttu-id="59469-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59469-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="59469-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="59469-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59469-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="59469-129">See also</span></span>



[<span data-ttu-id="59469-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="59469-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59469-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="59469-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59469-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="59469-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59469-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="59469-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

