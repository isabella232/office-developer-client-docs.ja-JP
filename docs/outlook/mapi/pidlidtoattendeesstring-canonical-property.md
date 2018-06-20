---
title: PidLidToAttendeesString の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c4daa46bf7c40f717f2bcd4a9ea87195f3d2c81f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802269"
---
# <a name="pidlidtoattendeesstring-canonical-property"></a><span data-ttu-id="294f1-103">PidLidToAttendeesString の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="294f1-103">PidLidToAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="294f1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="294f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="294f1-105">出席者全員のうっかりしているユーザーも必須出席者の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="294f1-105">Contains a list of all the sendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="294f1-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="294f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="294f1-107">dispidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="294f1-107">dispidToAttendeesString</span></span>  <br/> |
|<span data-ttu-id="294f1-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="294f1-108">Property set:</span></span>  <br/> |<span data-ttu-id="294f1-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="294f1-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="294f1-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="294f1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="294f1-111">0x0000823B</span><span class="sxs-lookup"><span data-stu-id="294f1-111">0x0000823B</span></span>  <br/> |
|<span data-ttu-id="294f1-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="294f1-112">Data type:</span></span>  <br/> |<span data-ttu-id="294f1-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="294f1-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="294f1-114">領域:</span><span class="sxs-lookup"><span data-stu-id="294f1-114">Area:</span></span>  <br/> |<span data-ttu-id="294f1-115">会議</span><span class="sxs-lookup"><span data-stu-id="294f1-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="294f1-116">備考</span><span class="sxs-lookup"><span data-stu-id="294f1-116">Remarks</span></span>

<span data-ttu-id="294f1-117">各出席者の値は、出席者のアドレス帳の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="294f1-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="294f1-118">別のエントリは、スペースの後にセミコロンで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="294f1-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="294f1-119">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="294f1-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="294f1-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="294f1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="294f1-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="294f1-121">Protocol specifications</span></span>

<span data-ttu-id="294f1-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="294f1-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="294f1-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="294f1-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="294f1-124">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="294f1-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="294f1-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="294f1-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="294f1-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="294f1-126">Header files</span></span>

<span data-ttu-id="294f1-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="294f1-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="294f1-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="294f1-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="294f1-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="294f1-129">See also</span></span>



[<span data-ttu-id="294f1-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="294f1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="294f1-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="294f1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="294f1-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="294f1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="294f1-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="294f1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

