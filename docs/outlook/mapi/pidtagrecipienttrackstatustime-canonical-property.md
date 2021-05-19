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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2dec706252eb6aa1b28f68f6f46473df04f3fbe7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355637"
---
# <a name="pidtagrecipienttrackstatustime-canonical-property"></a><span data-ttu-id="c28a8-103">PidTagRecipientTrackStatusTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c28a8-103">PidTagRecipientTrackStatusTime Canonical Property</span></span>

  
  
<span data-ttu-id="c28a8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c28a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c28a8-105">出席者が応答した日時を格納します。</span><span class="sxs-lookup"><span data-stu-id="c28a8-105">Contains the date and time when the attendee responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c28a8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c28a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c28a8-107">PR_RECIPIENT_TRACKSTATUS_TIME</span><span class="sxs-lookup"><span data-stu-id="c28a8-107">PR_RECIPIENT_TRACKSTATUS_TIME</span></span>  <br/> |
|<span data-ttu-id="c28a8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c28a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c28a8-109">0x5FFB</span><span class="sxs-lookup"><span data-stu-id="c28a8-109">0x5FFB</span></span>  <br/> |
|<span data-ttu-id="c28a8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c28a8-110">Data type:</span></span>  <br/> |<span data-ttu-id="c28a8-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c28a8-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c28a8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c28a8-112">Area:</span></span>  <br/> |<span data-ttu-id="c28a8-113">トランスポート受信者</span><span class="sxs-lookup"><span data-stu-id="c28a8-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c28a8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c28a8-114">Remarks</span></span>

<span data-ttu-id="c28a8-115">値は協定世界時 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c28a8-115">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c28a8-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c28a8-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c28a8-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c28a8-117">Protocol specifications</span></span>

<span data-ttu-id="c28a8-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c28a8-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c28a8-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="c28a8-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c28a8-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c28a8-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c28a8-121">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c28a8-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c28a8-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c28a8-122">Header files</span></span>

<span data-ttu-id="c28a8-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c28a8-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c28a8-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c28a8-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c28a8-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c28a8-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c28a8-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c28a8-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c28a8-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c28a8-127">See also</span></span>



[<span data-ttu-id="c28a8-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c28a8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c28a8-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c28a8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c28a8-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c28a8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c28a8-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c28a8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

