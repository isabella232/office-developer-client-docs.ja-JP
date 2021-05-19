---
title: PidTagReportDisposition 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 56b9e7bd-eece-4264-8ee5-a1bcbec4f35c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dae31959cddad7ad61ea32f2372ea34bdbff658e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423707"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="4a093-103">PidTagReportDisposition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a093-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="4a093-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a093-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a093-105">受信を要求するメッセージの受信状態を示します。</span><span class="sxs-lookup"><span data-stu-id="4a093-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a093-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4a093-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a093-107">PR_REPORT_DISPOSITION、PR_REPORT_DISPOSITION_A、PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="4a093-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="4a093-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4a093-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a093-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="4a093-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="4a093-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4a093-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a093-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4a093-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4a093-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4a093-112">Area:</span></span>  <br/> |<span data-ttu-id="4a093-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="4a093-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a093-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4a093-114">Remarks</span></span>

<span data-ttu-id="4a093-115">有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4a093-115">The following are valid values:</span></span>
  
- <span data-ttu-id="4a093-116">"deleted"</span><span class="sxs-lookup"><span data-stu-id="4a093-116">"deleted"</span></span>
    
- <span data-ttu-id="4a093-117">"処理"</span><span class="sxs-lookup"><span data-stu-id="4a093-117">"processed"</span></span>
    
- <span data-ttu-id="4a093-118">"dispatched"</span><span class="sxs-lookup"><span data-stu-id="4a093-118">"dispatched"</span></span>
    
- <span data-ttu-id="4a093-119">"denied"</span><span class="sxs-lookup"><span data-stu-id="4a093-119">"denied"</span></span>
    
- <span data-ttu-id="4a093-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="4a093-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="4a093-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4a093-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a093-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4a093-122">Protocol specifications</span></span>

<span data-ttu-id="4a093-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="4a093-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="4a093-124">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="4a093-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a093-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4a093-125">Header files</span></span>

<span data-ttu-id="4a093-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a093-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a093-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4a093-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a093-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4a093-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4a093-129">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="4a093-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a093-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="4a093-130">See also</span></span>



[<span data-ttu-id="4a093-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4a093-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a093-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a093-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a093-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="4a093-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a093-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="4a093-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

