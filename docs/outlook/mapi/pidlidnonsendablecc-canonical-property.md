---
title: PidLidNonSendableCc の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3f4859e4a354d83f62ca8fefa48f932425e2fc3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802051"
---
# <a name="pidlidnonsendablecc-canonical-property"></a><span data-ttu-id="05708-103">PidLidNonSendableCc の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="05708-103">PidLidNonSendableCc Canonical Property</span></span>

  
  
<span data-ttu-id="05708-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="05708-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="05708-105">すべての連絡先である出席者も任意出席者の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="05708-105">Contains a list of all the unsendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05708-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="05708-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05708-107">dispidNonSendableCC</span><span class="sxs-lookup"><span data-stu-id="05708-107">dispidNonSendableCC</span></span>  <br/> |
|<span data-ttu-id="05708-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="05708-108">Property set:</span></span>  <br/> |<span data-ttu-id="05708-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="05708-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="05708-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="05708-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="05708-111">0x00008537</span><span class="sxs-lookup"><span data-stu-id="05708-111">0x00008537</span></span>  <br/> |
|<span data-ttu-id="05708-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="05708-112">Data type:</span></span>  <br/> |<span data-ttu-id="05708-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="05708-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="05708-114">領域:</span><span class="sxs-lookup"><span data-stu-id="05708-114">Area:</span></span>  <br/> |<span data-ttu-id="05708-115">会議</span><span class="sxs-lookup"><span data-stu-id="05708-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05708-116">備考</span><span class="sxs-lookup"><span data-stu-id="05708-116">Remarks</span></span>

<span data-ttu-id="05708-117">各出席者の値は、出席者のアドレス帳の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="05708-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="05708-118">別のエントリは、スペースの後にセミコロンで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="05708-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="05708-119">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="05708-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="05708-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="05708-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05708-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="05708-121">Protocol specifications</span></span>

<span data-ttu-id="05708-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05708-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05708-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="05708-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="05708-124">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05708-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05708-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="05708-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="05708-126">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05708-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05708-127">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="05708-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05708-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="05708-128">Header files</span></span>

<span data-ttu-id="05708-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05708-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="05708-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="05708-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05708-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="05708-131">See also</span></span>



[<span data-ttu-id="05708-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="05708-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05708-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="05708-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05708-134">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="05708-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05708-135">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="05708-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

