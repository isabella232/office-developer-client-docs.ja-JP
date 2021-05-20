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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d598337a4a66b6345b2f7c827b62a2ccd8af366
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428971"
---
# <a name="pidtagreportdispositionmode-canonical-property"></a><span data-ttu-id="703e1-103">PidTagReportDispositionMode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="703e1-103">PidTagReportDispositionMode Canonical Property</span></span>

  
  
<span data-ttu-id="703e1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="703e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="703e1-105">受信を要求するメッセージの受信の廃棄を示します。</span><span class="sxs-lookup"><span data-stu-id="703e1-105">Indicates the disposition of the receipt for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="703e1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="703e1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="703e1-107">PR_REPORT_DISPOSITION_MODE、PR_REPORT_DISPOSITION_MODE_A、PR_REPORT_DISPOSITION_MODE_W</span><span class="sxs-lookup"><span data-stu-id="703e1-107">PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W</span></span>  <br/> |
|<span data-ttu-id="703e1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="703e1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="703e1-109">0x0081</span><span class="sxs-lookup"><span data-stu-id="703e1-109">0x0081</span></span>  <br/> |
|<span data-ttu-id="703e1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="703e1-110">Data type:</span></span>  <br/> |<span data-ttu-id="703e1-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="703e1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="703e1-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="703e1-112">Area:</span></span>  <br/> |<span data-ttu-id="703e1-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="703e1-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="703e1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="703e1-114">Remarks</span></span>

<span data-ttu-id="703e1-115">このプロパティに使用できる値は、「手動アクション/MDN-sent-automatically」と「手動アクション/MDN-sent-manually」です。</span><span class="sxs-lookup"><span data-stu-id="703e1-115">The possible values for this property are "manual-action/MDN-sent-automatically" and "manual-action/MDN-sent-manually".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="703e1-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="703e1-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="703e1-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="703e1-117">Protocol specifications</span></span>

<span data-ttu-id="703e1-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="703e1-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="703e1-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="703e1-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="703e1-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="703e1-120">Header files</span></span>

<span data-ttu-id="703e1-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="703e1-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="703e1-122">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="703e1-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="703e1-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="703e1-123">Mapitags.h</span></span>
  
> <span data-ttu-id="703e1-124">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="703e1-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="703e1-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="703e1-125">See also</span></span>



[<span data-ttu-id="703e1-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="703e1-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="703e1-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="703e1-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="703e1-128">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="703e1-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="703e1-129">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="703e1-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

