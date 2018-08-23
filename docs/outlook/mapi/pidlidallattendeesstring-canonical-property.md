---
title: PidLidAllAttendeesString 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAllAttendeesString
api_type:
- COM
ms.assetid: 2ffc0609-341d-4e35-8f53-ed3096c6fa7f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a9580428cd985902d3af6320dd754947565b74e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801722"
---
# <a name="pidlidallattendeesstring-canonical-property"></a><span data-ttu-id="0df27-103">PidLidAllAttendeesString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0df27-103">PidLidAllAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="0df27-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0df27-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0df27-105">リソースと連絡先の参加者を含め、開催者以外のすべての出席者の一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="0df27-105">Specifies a list of all the attendees except for the organizer, including resources and unsendable attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0df27-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0df27-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0df27-107">dispidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="0df27-107">dispidAllAttendeesString</span></span>  <br/> |
|<span data-ttu-id="0df27-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0df27-108">Property set:</span></span>  <br/> |<span data-ttu-id="0df27-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0df27-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0df27-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0df27-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0df27-111">0x00008238</span><span class="sxs-lookup"><span data-stu-id="0df27-111">0x00008238</span></span>  <br/> |
|<span data-ttu-id="0df27-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0df27-112">Data type:</span></span>  <br/> |<span data-ttu-id="0df27-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0df27-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0df27-114">領域:</span><span class="sxs-lookup"><span data-stu-id="0df27-114">Area:</span></span>  <br/> |<span data-ttu-id="0df27-115">会議</span><span class="sxs-lookup"><span data-stu-id="0df27-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0df27-116">注釈</span><span class="sxs-lookup"><span data-stu-id="0df27-116">Remarks</span></span>

<span data-ttu-id="0df27-117">各出席者の値は、出席者の表示名です。</span><span class="sxs-lookup"><span data-stu-id="0df27-117">The value for each attendee is the attendee's display name.</span></span> <span data-ttu-id="0df27-118">別のエントリは、スペースの後にセミコロンで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="0df27-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="0df27-119">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="0df27-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0df27-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0df27-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0df27-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0df27-121">Protocol specifications</span></span>

<span data-ttu-id="0df27-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0df27-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0df27-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0df27-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0df27-124">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0df27-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0df27-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0df27-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0df27-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0df27-126">Header files</span></span>

<span data-ttu-id="0df27-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0df27-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0df27-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0df27-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0df27-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="0df27-129">See also</span></span>



[<span data-ttu-id="0df27-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0df27-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0df27-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0df27-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0df27-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0df27-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0df27-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0df27-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

