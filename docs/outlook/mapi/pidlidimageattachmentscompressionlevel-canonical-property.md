---
title: PidLidImageAttachmentsCompressionLevel の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidImageAttachmentsCompressionLevel
api_type:
- COM
ms.assetid: cc169ba8-e9b7-42ad-8f0e-77b0843f95ea
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 13e2ac93e7e3ba46bf25b26e76bd44c15f2b89e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802001"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="fc6dd-103">PidLidImageAttachmentsCompressionLevel の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="fc6dd-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="fc6dd-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc6dd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc6dd-105">画像添付ファイルに適用する圧縮のレベルを定義します。</span><span class="sxs-lookup"><span data-stu-id="fc6dd-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc6dd-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="fc6dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc6dd-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="fc6dd-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="fc6dd-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="fc6dd-108">Property set:</span></span>  <br/> |<span data-ttu-id="fc6dd-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fc6dd-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fc6dd-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fc6dd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fc6dd-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="fc6dd-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="fc6dd-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="fc6dd-112">Data type:</span></span>  <br/> |<span data-ttu-id="fc6dd-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fc6dd-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fc6dd-114">領域:</span><span class="sxs-lookup"><span data-stu-id="fc6dd-114">Area:</span></span>  <br/> |<span data-ttu-id="fc6dd-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="fc6dd-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc6dd-116">備考</span><span class="sxs-lookup"><span data-stu-id="fc6dd-116">Remarks</span></span>

<span data-ttu-id="fc6dd-117">有効な圧縮レベルは、次のように。</span><span class="sxs-lookup"><span data-stu-id="fc6dd-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="fc6dd-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fc6dd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc6dd-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fc6dd-119">Protocol specifications</span></span>

<span data-ttu-id="fc6dd-120">[MS OXPROPS]</span><span class="sxs-lookup"><span data-stu-id="fc6dd-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="fc6dd-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fc6dd-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc6dd-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fc6dd-122">Header files</span></span>

<span data-ttu-id="fc6dd-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc6dd-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc6dd-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fc6dd-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc6dd-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc6dd-125">See also</span></span>



[<span data-ttu-id="fc6dd-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fc6dd-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc6dd-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fc6dd-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc6dd-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="fc6dd-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc6dd-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="fc6dd-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

