---
title: PidTagAlternateRecipientAllowed の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: dc77f9c7b58fc925048d6dec2bee2ff96a8723b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802447"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="b7115-103">PidTagAlternateRecipientAllowed の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b7115-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="b7115-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7115-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7115-105">送信者はこのメッセージの自動転送を許可している場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="b7115-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7115-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b7115-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7115-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="b7115-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="b7115-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b7115-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b7115-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="b7115-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="b7115-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="b7115-110">Data type:</span></span>  <br/> |<span data-ttu-id="b7115-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b7115-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b7115-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b7115-112">Area:</span></span>  <br/> |<span data-ttu-id="b7115-113">Address</span><span class="sxs-lookup"><span data-stu-id="b7115-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7115-114">備考</span><span class="sxs-lookup"><span data-stu-id="b7115-114">Remarks</span></span>

<span data-ttu-id="b7115-115">自動転送が許可されていない場合、または別の受信者が指定されていない場合は、配信不能レポートを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7115-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b7115-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b7115-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7115-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b7115-117">Protocol specifications</span></span>

<span data-ttu-id="b7115-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7115-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7115-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7115-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7115-120">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7115-120">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7115-121">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="b7115-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="b7115-122">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7115-122">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7115-123">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="b7115-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b7115-124">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7115-124">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7115-125">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="b7115-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7115-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b7115-126">Header files</span></span>

<span data-ttu-id="b7115-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7115-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7115-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7115-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="b7115-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b7115-129">Mapitags.h</span></span>
  
> <span data-ttu-id="b7115-130">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b7115-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7115-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7115-131">See also</span></span>



[<span data-ttu-id="b7115-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7115-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7115-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7115-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7115-134">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="b7115-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7115-135">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="b7115-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

