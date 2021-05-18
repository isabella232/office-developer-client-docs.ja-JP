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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7b7cfe1fc1068e5b5b228c4de4c9317d9bcbbc66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328736"
---
# <a name="pidlidnonsendablebcc-canonical-property"></a><span data-ttu-id="64783-103">PidLidNonSendableBcc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="64783-103">PidLidNonSendableBcc Canonical Property</span></span>

  
  
<span data-ttu-id="64783-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64783-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64783-105">リソースである、送信できないすべての出席者の一覧が含まれる。</span><span class="sxs-lookup"><span data-stu-id="64783-105">Contains a list of all the unsendable attendees who are resources.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64783-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="64783-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64783-107">dispidNonSendableBCC</span><span class="sxs-lookup"><span data-stu-id="64783-107">dispidNonSendableBCC</span></span>  <br/> |
|<span data-ttu-id="64783-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="64783-108">Property set:</span></span>  <br/> |<span data-ttu-id="64783-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="64783-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="64783-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="64783-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="64783-111">0x00008538</span><span class="sxs-lookup"><span data-stu-id="64783-111">0x00008538</span></span>  <br/> |
|<span data-ttu-id="64783-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="64783-112">Data type:</span></span>  <br/> |<span data-ttu-id="64783-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="64783-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="64783-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="64783-114">Area:</span></span>  <br/> |<span data-ttu-id="64783-115">会議</span><span class="sxs-lookup"><span data-stu-id="64783-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64783-116">注釈</span><span class="sxs-lookup"><span data-stu-id="64783-116">Remarks</span></span>

<span data-ttu-id="64783-117">各出席者の値は、PR_DISPLAY_NAME **の** アドレス帳のプロパティ ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) です。</span><span class="sxs-lookup"><span data-stu-id="64783-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="64783-118">個別のエントリは、セミコロンで区切り、その後にスペースを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64783-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="64783-119">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="64783-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="64783-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="64783-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64783-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="64783-121">Protocol specifications</span></span>

<span data-ttu-id="64783-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64783-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64783-123">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="64783-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64783-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64783-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64783-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="64783-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="64783-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64783-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64783-127">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="64783-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64783-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="64783-128">Header files</span></span>

<span data-ttu-id="64783-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64783-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="64783-130">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="64783-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64783-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="64783-131">See also</span></span>



[<span data-ttu-id="64783-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="64783-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64783-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="64783-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64783-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="64783-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64783-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="64783-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

