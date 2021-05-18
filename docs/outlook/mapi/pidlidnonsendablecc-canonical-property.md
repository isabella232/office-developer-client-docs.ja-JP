---
title: PidLidNonSendableCc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableCc
api_type:
- COM
ms.assetid: 170afe1f-1223-4689-825c-d21ab14b213b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d9f166b0d1e180fdb087fbf602e6841c3fdac3dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319657"
---
# <a name="pidlidnonsendablecc-canonical-property"></a><span data-ttu-id="d9f0d-103">PidLidNonSendableCc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9f0d-103">PidLidNonSendableCc Canonical Property</span></span>

  
  
<span data-ttu-id="d9f0d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9f0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9f0d-105">省略可能な出席者である、すべての送信不可の出席者の一覧が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d9f0d-105">Contains a list of all the unsendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9f0d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d9f0d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9f0d-107">dispidNonSendableCC</span><span class="sxs-lookup"><span data-stu-id="d9f0d-107">dispidNonSendableCC</span></span>  <br/> |
|<span data-ttu-id="d9f0d-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="d9f0d-108">Property set:</span></span>  <br/> |<span data-ttu-id="d9f0d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d9f0d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d9f0d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d9f0d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d9f0d-111">0x00008537</span><span class="sxs-lookup"><span data-stu-id="d9f0d-111">0x00008537</span></span>  <br/> |
|<span data-ttu-id="d9f0d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d9f0d-112">Data type:</span></span>  <br/> |<span data-ttu-id="d9f0d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d9f0d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d9f0d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="d9f0d-114">Area:</span></span>  <br/> |<span data-ttu-id="d9f0d-115">会議</span><span class="sxs-lookup"><span data-stu-id="d9f0d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9f0d-116">注釈</span><span class="sxs-lookup"><span data-stu-id="d9f0d-116">Remarks</span></span>

<span data-ttu-id="d9f0d-117">各出席者の値は、PR_DISPLAY_NAME **の** アドレス帳のプロパティ ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) です。</span><span class="sxs-lookup"><span data-stu-id="d9f0d-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="d9f0d-118">個別のエントリは、セミコロンで区切り、その後にスペースを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9f0d-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="d9f0d-119">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="d9f0d-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d9f0d-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d9f0d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9f0d-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d9f0d-121">Protocol specifications</span></span>

<span data-ttu-id="d9f0d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9f0d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9f0d-123">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="d9f0d-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9f0d-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9f0d-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9f0d-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d9f0d-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="d9f0d-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9f0d-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9f0d-127">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="d9f0d-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9f0d-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d9f0d-128">Header files</span></span>

<span data-ttu-id="d9f0d-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9f0d-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9f0d-130">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d9f0d-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9f0d-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9f0d-131">See also</span></span>



[<span data-ttu-id="d9f0d-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d9f0d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9f0d-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9f0d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9f0d-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d9f0d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9f0d-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d9f0d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

