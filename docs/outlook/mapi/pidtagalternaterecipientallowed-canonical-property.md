---
title: PidTagAlternateRecipientAllowed 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipientAllowed
api_type:
- HeaderDef
ms.assetid: dbbdeb54-3d14-4601-a77b-55ee31f33416
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0faeb12ee54ec5d1c584bacd51590b157035f4fd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385958"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="e310a-103">PidTagAlternateRecipientAllowed 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e310a-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="e310a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e310a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e310a-105">送信者はこのメッセージの自動転送を許可している場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="e310a-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e310a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e310a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e310a-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="e310a-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="e310a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e310a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e310a-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="e310a-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="e310a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e310a-110">Data type:</span></span>  <br/> |<span data-ttu-id="e310a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e310a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e310a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e310a-112">Area:</span></span>  <br/> |<span data-ttu-id="e310a-113">Address</span><span class="sxs-lookup"><span data-stu-id="e310a-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e310a-114">備考</span><span class="sxs-lookup"><span data-stu-id="e310a-114">Remarks</span></span>

<span data-ttu-id="e310a-115">自動転送が許可されていない場合、または別の受信者が指定されていない場合は、配信不能レポートを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e310a-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e310a-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e310a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e310a-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e310a-117">Protocol specifications</span></span>

<span data-ttu-id="e310a-118">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e310a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e310a-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e310a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e310a-120">[[MS OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e310a-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e310a-121">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="e310a-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e310a-122">[[MS OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e310a-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e310a-123">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="e310a-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e310a-124">[[MS OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e310a-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e310a-125">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="e310a-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e310a-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e310a-126">Header files</span></span>

<span data-ttu-id="e310a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e310a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e310a-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e310a-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="e310a-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e310a-129">Mapitags.h</span></span>
  
> <span data-ttu-id="e310a-130">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e310a-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e310a-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="e310a-131">See also</span></span>



[<span data-ttu-id="e310a-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e310a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e310a-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e310a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e310a-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e310a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e310a-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e310a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

