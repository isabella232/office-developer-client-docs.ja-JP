---
title: PidLidFExceptionalAttendees の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalAttendees
api_type:
- COM
ms.assetid: f1f489a3-e83a-4e96-bf9a-d98bc17d29f5
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7c7f654d42df7856b0e69bf276a763ccd29d1d87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801961"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a><span data-ttu-id="b00fa-103">PidLidFExceptionalAttendees の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b00fa-103">PidLidFExceptionalAttendees Canonical Property</span></span>

  
  
<span data-ttu-id="b00fa-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b00fa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b00fa-105">このプロパティは、1 つまたは複数の例外の定期的な予定表オブジェクトを少なくとも 1 つの RecipientRow には、埋め込まれている例外メッセージの少なくとも 1 つかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b00fa-105">Indicates whether this property is a recurring calendar object with one or more exceptions, and at least one of the exception embedded messages has at least one RecipientRow.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b00fa-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b00fa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b00fa-107">dispidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="b00fa-107">dispidFExceptionalAttendees</span></span>  <br/> |
|<span data-ttu-id="b00fa-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b00fa-108">Property set:</span></span>  <br/> |<span data-ttu-id="b00fa-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b00fa-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b00fa-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b00fa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b00fa-111">0x0000822B</span><span class="sxs-lookup"><span data-stu-id="b00fa-111">0x0000822B</span></span>  <br/> |
|<span data-ttu-id="b00fa-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="b00fa-112">Data type:</span></span>  <br/> |<span data-ttu-id="b00fa-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b00fa-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b00fa-114">領域:</span><span class="sxs-lookup"><span data-stu-id="b00fa-114">Area:</span></span>  <br/> |<span data-ttu-id="b00fa-115">会議</span><span class="sxs-lookup"><span data-stu-id="b00fa-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b00fa-116">備考</span><span class="sxs-lookup"><span data-stu-id="b00fa-116">Remarks</span></span>

<span data-ttu-id="b00fa-117">値の false の場合、または、このプロパティがない場合は、カレンダー オブジェクトが例外を含んでいないか、または埋め込まれている例外メッセージは、RecipientRows のことを示します。</span><span class="sxs-lookup"><span data-stu-id="b00fa-117">A value of FALSE, or the absence of this property, indicates that the calendar object either has no exceptions, or none of the exception embedded messages has RecipientRows.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b00fa-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b00fa-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b00fa-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b00fa-119">Protocol specifications</span></span>

<span data-ttu-id="b00fa-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b00fa-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b00fa-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b00fa-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b00fa-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b00fa-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b00fa-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b00fa-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b00fa-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b00fa-124">Header files</span></span>

<span data-ttu-id="b00fa-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b00fa-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b00fa-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b00fa-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b00fa-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="b00fa-127">See also</span></span>



[<span data-ttu-id="b00fa-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b00fa-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b00fa-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b00fa-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b00fa-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="b00fa-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b00fa-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="b00fa-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

