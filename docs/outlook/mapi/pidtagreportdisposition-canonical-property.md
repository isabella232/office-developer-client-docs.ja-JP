---
title: PidTagReportDisposition の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 56b9e7bd-eece-4264-8ee5-a1bcbec4f35c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 62d5b04086e45b6b3d2cfa960472010827d60d6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803344"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="6db3f-103">PidTagReportDisposition の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6db3f-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="6db3f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6db3f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6db3f-105">領収書を要求するメッセージの受信確認状況を示します。</span><span class="sxs-lookup"><span data-stu-id="6db3f-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6db3f-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="6db3f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6db3f-107">PR_REPORT_DISPOSITION、PR_REPORT_DISPOSITION_A、PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="6db3f-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="6db3f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6db3f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6db3f-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="6db3f-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="6db3f-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="6db3f-110">Data type:</span></span>  <br/> |<span data-ttu-id="6db3f-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6db3f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6db3f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6db3f-112">Area:</span></span>  <br/> |<span data-ttu-id="6db3f-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="6db3f-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6db3f-114">備考</span><span class="sxs-lookup"><span data-stu-id="6db3f-114">Remarks</span></span>

<span data-ttu-id="6db3f-115">有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6db3f-115">The following are valid values:</span></span>
  
- <span data-ttu-id="6db3f-116">「削除」</span><span class="sxs-lookup"><span data-stu-id="6db3f-116">"deleted"</span></span>
    
- <span data-ttu-id="6db3f-117">「処理」</span><span class="sxs-lookup"><span data-stu-id="6db3f-117">"processed"</span></span>
    
- <span data-ttu-id="6db3f-118">「ディスパッチ」</span><span class="sxs-lookup"><span data-stu-id="6db3f-118">"dispatched"</span></span>
    
- <span data-ttu-id="6db3f-119">「拒否」</span><span class="sxs-lookup"><span data-stu-id="6db3f-119">"denied"</span></span>
    
- <span data-ttu-id="6db3f-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="6db3f-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="6db3f-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6db3f-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6db3f-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6db3f-122">Protocol specifications</span></span>

<span data-ttu-id="6db3f-123">[MS OXPROPS]</span><span class="sxs-lookup"><span data-stu-id="6db3f-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="6db3f-124">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6db3f-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6db3f-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6db3f-125">Header files</span></span>

<span data-ttu-id="6db3f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6db3f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6db3f-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6db3f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="6db3f-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6db3f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="6db3f-129">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6db3f-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6db3f-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="6db3f-130">See also</span></span>



[<span data-ttu-id="6db3f-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6db3f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6db3f-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6db3f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6db3f-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="6db3f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6db3f-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="6db3f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

