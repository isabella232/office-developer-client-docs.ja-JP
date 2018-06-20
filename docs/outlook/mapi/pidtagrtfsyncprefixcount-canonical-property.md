---
title: PidTagRtfSyncPrefixCount の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncPrefixCount
api_type:
- COM
ms.assetid: c2b15ac5-9e89-4ee2-812d-102d0b2ac56e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c9a62365b46e85cc8f5d22fd31de3b5c6bd3f76a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803387"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="fb73b-103">PidTagRtfSyncPrefixCount の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="fb73b-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="fb73b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb73b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb73b-105">メッセージの重要な文字の前に表示される無視可能な文字の数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fb73b-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fb73b-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="fb73b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fb73b-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="fb73b-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="fb73b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fb73b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fb73b-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="fb73b-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="fb73b-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="fb73b-110">Data type:</span></span>  <br/> |<span data-ttu-id="fb73b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fb73b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fb73b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="fb73b-112">Area:</span></span>  <br/> |<span data-ttu-id="fb73b-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="fb73b-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb73b-114">備考</span><span class="sxs-lookup"><span data-stu-id="fb73b-114">Remarks</span></span>

<span data-ttu-id="fb73b-115">プレフィックス文字の数では、ホワイト スペースは含まれません。</span><span class="sxs-lookup"><span data-stu-id="fb73b-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="fb73b-116">このプロパティは、リッチ テキスト形式 (RTF) 補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="fb73b-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="fb73b-117">RTF の補助プロパティでは、[行う](rtfsync.md)関数によって使用され、クライアント アプリケーションで直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="fb73b-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fb73b-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fb73b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fb73b-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fb73b-119">Protocol specifications</span></span>

<span data-ttu-id="fb73b-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb73b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb73b-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fb73b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fb73b-122">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb73b-122">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb73b-123">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="fb73b-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fb73b-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fb73b-124">Header files</span></span>

<span data-ttu-id="fb73b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb73b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fb73b-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fb73b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="fb73b-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fb73b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="fb73b-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fb73b-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb73b-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="fb73b-129">See also</span></span>



[<span data-ttu-id="fb73b-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fb73b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fb73b-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fb73b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fb73b-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="fb73b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fb73b-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="fb73b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

