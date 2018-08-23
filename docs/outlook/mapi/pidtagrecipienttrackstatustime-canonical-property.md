---
title: PidTagRecipientTrackStatusTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatusTime
api_type:
- COM
ms.assetid: f14dfe47-a9f8-4475-bb26-7da3411d8c6f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0db4efcf1e05536ee7abb3459caa0159f84ef798
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803293"
---
# <a name="pidtagrecipienttrackstatustime-canonical-property"></a><span data-ttu-id="21a53-103">PidTagRecipientTrackStatusTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="21a53-103">PidTagRecipientTrackStatusTime Canonical Property</span></span>

  
  
<span data-ttu-id="21a53-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="21a53-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="21a53-105">出席者が反応したときの日時が含まれています。</span><span class="sxs-lookup"><span data-stu-id="21a53-105">Contains the date and time when the attendee responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21a53-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="21a53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="21a53-107">PR_RECIPIENT_TRACKSTATUS_TIME</span><span class="sxs-lookup"><span data-stu-id="21a53-107">PR_RECIPIENT_TRACKSTATUS_TIME</span></span>  <br/> |
|<span data-ttu-id="21a53-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="21a53-108">Identifier:</span></span>  <br/> |<span data-ttu-id="21a53-109">0x5FFB</span><span class="sxs-lookup"><span data-stu-id="21a53-109">0x5FFB</span></span>  <br/> |
|<span data-ttu-id="21a53-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="21a53-110">Data type:</span></span>  <br/> |<span data-ttu-id="21a53-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="21a53-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="21a53-112">領域:</span><span class="sxs-lookup"><span data-stu-id="21a53-112">Area:</span></span>  <br/> |<span data-ttu-id="21a53-113">トランスポートにおける受取人</span><span class="sxs-lookup"><span data-stu-id="21a53-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21a53-114">注釈</span><span class="sxs-lookup"><span data-stu-id="21a53-114">Remarks</span></span>

<span data-ttu-id="21a53-115">値は、世界協定時刻 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21a53-115">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="21a53-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="21a53-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="21a53-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="21a53-117">Protocol specifications</span></span>

<span data-ttu-id="21a53-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21a53-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21a53-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="21a53-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="21a53-120">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21a53-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21a53-121">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="21a53-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="21a53-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="21a53-122">Header files</span></span>

<span data-ttu-id="21a53-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="21a53-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="21a53-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="21a53-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="21a53-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="21a53-125">Mapitags.h</span></span>
  
> <span data-ttu-id="21a53-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="21a53-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21a53-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="21a53-127">See also</span></span>



[<span data-ttu-id="21a53-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="21a53-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="21a53-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="21a53-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="21a53-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="21a53-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="21a53-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="21a53-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

