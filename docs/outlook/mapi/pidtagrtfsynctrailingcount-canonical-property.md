---
title: PidTagRtfSyncTrailingCount の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncTrailingCount
api_type:
- COM
ms.assetid: 3f0e5b24-767e-46f5-bb3d-e9cb82cb935b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3174ebbcf70104c82305e2a20df1e183d30265d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803389"
---
# <a name="pidtagrtfsynctrailingcount-canonical-property"></a><span data-ttu-id="c6ea0-103">PidTagRtfSyncTrailingCount の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="c6ea0-103">PidTagRtfSyncTrailingCount Canonical Property</span></span>

  
  
<span data-ttu-id="c6ea0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6ea0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c6ea0-105">メッセージの重要な文字の後に表示される、無視できる文字の数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c6ea0-105">Contains a count of the ignorable characters that appear after the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c6ea0-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="c6ea0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c6ea0-107">PR_RTF_SYNC_TRAILING_COUNT</span><span class="sxs-lookup"><span data-stu-id="c6ea0-107">PR_RTF_SYNC_TRAILING_COUNT</span></span>  <br/> |
|<span data-ttu-id="c6ea0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c6ea0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c6ea0-109">0x1011</span><span class="sxs-lookup"><span data-stu-id="c6ea0-109">0x1011</span></span>  <br/> |
|<span data-ttu-id="c6ea0-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="c6ea0-110">Data type:</span></span>  <br/> |<span data-ttu-id="c6ea0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c6ea0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c6ea0-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c6ea0-112">Area:</span></span>  <br/> |<span data-ttu-id="c6ea0-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="c6ea0-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6ea0-114">備考</span><span class="sxs-lookup"><span data-stu-id="c6ea0-114">Remarks</span></span>

<span data-ttu-id="c6ea0-115">このプロパティは、リッチ テキスト形式 (RFT) 補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="c6ea0-115">This property is a Rich Text Format (RFT) auxiliary property.</span></span> <span data-ttu-id="c6ea0-116">これらのプロパティ[へ](rtfsync.md)の関数で使用され、クライアント アプリケーションで直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="c6ea0-116">These properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c6ea0-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c6ea0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c6ea0-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c6ea0-118">Protocol specifications</span></span>

<span data-ttu-id="c6ea0-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6ea0-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6ea0-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c6ea0-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c6ea0-121">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6ea0-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6ea0-122">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="c6ea0-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c6ea0-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c6ea0-123">Header files</span></span>

<span data-ttu-id="c6ea0-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6ea0-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="c6ea0-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c6ea0-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="c6ea0-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c6ea0-126">Mapitags.h</span></span>
  
> <span data-ttu-id="c6ea0-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c6ea0-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6ea0-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="c6ea0-128">See also</span></span>



[<span data-ttu-id="c6ea0-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c6ea0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c6ea0-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c6ea0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c6ea0-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="c6ea0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c6ea0-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="c6ea0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

