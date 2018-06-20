---
title: PidTagReportDispositionMode の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 67b3c76a-f6f7-462b-955c-dc7b53e7e7eb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bc2d577ad6c6b430c2339dfb0567ca56de0a7f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803340"
---
# <a name="pidtagreportdispositionmode-canonical-property"></a><span data-ttu-id="3bd5b-103">PidTagReportDispositionMode の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="3bd5b-103">PidTagReportDispositionMode Canonical Property</span></span>

  
  
<span data-ttu-id="3bd5b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3bd5b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3bd5b-105">領収書を要求するメッセージの受信確認の処理方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3bd5b-105">Indicates the disposition of the receipt for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3bd5b-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="3bd5b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3bd5b-107">PR_REPORT_DISPOSITION_MODE、PR_REPORT_DISPOSITION_MODE_A、PR_REPORT_DISPOSITION_MODE_W</span><span class="sxs-lookup"><span data-stu-id="3bd5b-107">PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W</span></span>  <br/> |
|<span data-ttu-id="3bd5b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3bd5b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3bd5b-109">0x0081</span><span class="sxs-lookup"><span data-stu-id="3bd5b-109">0x0081</span></span>  <br/> |
|<span data-ttu-id="3bd5b-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="3bd5b-110">Data type:</span></span>  <br/> |<span data-ttu-id="3bd5b-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3bd5b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3bd5b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="3bd5b-112">Area:</span></span>  <br/> |<span data-ttu-id="3bd5b-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="3bd5b-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bd5b-114">備考</span><span class="sxs-lookup"><span data-stu-id="3bd5b-114">Remarks</span></span>

<span data-ttu-id="3bd5b-115">このプロパティの有効な値は、「マニュアル-アクション/MDN の送信が自動的に手動の操作/MDN の送信-手動でします。</span><span class="sxs-lookup"><span data-stu-id="3bd5b-115">The possible values for this property are "manual-action/MDN-sent-automatically" and "manual-action/MDN-sent-manually".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3bd5b-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3bd5b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3bd5b-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3bd5b-117">Protocol specifications</span></span>

<span data-ttu-id="3bd5b-118">[MS OXPROPS]</span><span class="sxs-lookup"><span data-stu-id="3bd5b-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="3bd5b-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3bd5b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3bd5b-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3bd5b-120">Header files</span></span>

<span data-ttu-id="3bd5b-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3bd5b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="3bd5b-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3bd5b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="3bd5b-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3bd5b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="3bd5b-124">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3bd5b-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3bd5b-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="3bd5b-125">See also</span></span>



[<span data-ttu-id="3bd5b-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3bd5b-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3bd5b-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3bd5b-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3bd5b-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="3bd5b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3bd5b-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="3bd5b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

