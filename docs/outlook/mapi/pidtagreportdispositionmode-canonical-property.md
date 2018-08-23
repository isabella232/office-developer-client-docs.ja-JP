---
title: PidTagReportDispositionMode 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 67b3c76a-f6f7-462b-955c-dc7b53e7e7eb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bc2d577ad6c6b430c2339dfb0567ca56de0a7f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803340"
---
# <a name="pidtagreportdispositionmode-canonical-property"></a><span data-ttu-id="d84cf-103">PidTagReportDispositionMode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d84cf-103">PidTagReportDispositionMode Canonical Property</span></span>

  
  
<span data-ttu-id="d84cf-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d84cf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d84cf-105">領収書を要求するメッセージの受信確認の処理方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d84cf-105">Indicates the disposition of the receipt for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d84cf-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d84cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d84cf-107">PR_REPORT_DISPOSITION_MODE、PR_REPORT_DISPOSITION_MODE_A、PR_REPORT_DISPOSITION_MODE_W</span><span class="sxs-lookup"><span data-stu-id="d84cf-107">PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W</span></span>  <br/> |
|<span data-ttu-id="d84cf-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d84cf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d84cf-109">0x0081</span><span class="sxs-lookup"><span data-stu-id="d84cf-109">0x0081</span></span>  <br/> |
|<span data-ttu-id="d84cf-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d84cf-110">Data type:</span></span>  <br/> |<span data-ttu-id="d84cf-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d84cf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d84cf-112">領域:</span><span class="sxs-lookup"><span data-stu-id="d84cf-112">Area:</span></span>  <br/> |<span data-ttu-id="d84cf-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="d84cf-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d84cf-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d84cf-114">Remarks</span></span>

<span data-ttu-id="d84cf-115">このプロパティの有効な値は、「マニュアル-アクション/MDN の送信が自動的に手動の操作/MDN の送信-手動でします。</span><span class="sxs-lookup"><span data-stu-id="d84cf-115">The possible values for this property are "manual-action/MDN-sent-automatically" and "manual-action/MDN-sent-manually".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d84cf-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d84cf-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d84cf-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d84cf-117">Protocol specifications</span></span>

<span data-ttu-id="d84cf-118">[MS OXPROPS]</span><span class="sxs-lookup"><span data-stu-id="d84cf-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="d84cf-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d84cf-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d84cf-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d84cf-120">Header files</span></span>

<span data-ttu-id="d84cf-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d84cf-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="d84cf-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d84cf-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="d84cf-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d84cf-123">Mapitags.h</span></span>
  
> <span data-ttu-id="d84cf-124">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d84cf-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d84cf-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="d84cf-125">See also</span></span>



[<span data-ttu-id="d84cf-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d84cf-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d84cf-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d84cf-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d84cf-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d84cf-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d84cf-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d84cf-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

