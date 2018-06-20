---
title: PidTagOriginalMessageClass の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalMessageClass
api_type:
- COM
ms.assetid: 49deb153-03c6-4be2-a3a5-53cca01accba
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7167b7b51698cda5610356779a8e8342b34a6082
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803096"
---
# <a name="pidtagoriginalmessageclass-canonical-property"></a><span data-ttu-id="3e45e-103">PidTagOriginalMessageClass の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="3e45e-103">PidTagOriginalMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="3e45e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3e45e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3e45e-105">レポートで使用する元のメッセージのクラスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3e45e-105">Contains the class of the original message for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3e45e-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="3e45e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3e45e-107">PR_ORIG_MESSAGE_CLASS、PR_ORIG_MESSAGE_CLASS_A、PR_ORIG_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="3e45e-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="3e45e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3e45e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3e45e-109">0x004B</span><span class="sxs-lookup"><span data-stu-id="3e45e-109">0x004B</span></span>  <br/> |
|<span data-ttu-id="3e45e-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="3e45e-110">Data type:</span></span>  <br/> |<span data-ttu-id="3e45e-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3e45e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3e45e-112">領域:</span><span class="sxs-lookup"><span data-stu-id="3e45e-112">Area:</span></span>  <br/> |<span data-ttu-id="3e45e-113">メッセージング プロパティをセキュリティで保護します。</span><span class="sxs-lookup"><span data-stu-id="3e45e-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e45e-114">備考</span><span class="sxs-lookup"><span data-stu-id="3e45e-114">Remarks</span></span>

<span data-ttu-id="3e45e-115">これらのプロパティには、レポートが生成されるメッセージの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティのコピーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3e45e-115">These properties contain a copy of the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message for which the report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3e45e-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3e45e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3e45e-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3e45e-117">Protocol specifications</span></span>

<span data-ttu-id="3e45e-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e45e-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e45e-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3e45e-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3e45e-120">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e45e-120">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e45e-121">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="3e45e-121">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3e45e-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3e45e-122">Header files</span></span>

<span data-ttu-id="3e45e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3e45e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3e45e-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3e45e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3e45e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3e45e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="3e45e-126">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3e45e-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e45e-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e45e-127">See also</span></span>



[<span data-ttu-id="3e45e-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e45e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3e45e-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e45e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3e45e-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="3e45e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3e45e-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="3e45e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

