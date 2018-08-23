---
title: PidLidImageAttachmentsCompressionLevel 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 13e2ac93e7e3ba46bf25b26e76bd44c15f2b89e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802001"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="b4775-103">PidLidImageAttachmentsCompressionLevel 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b4775-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="b4775-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4775-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4775-105">画像添付ファイルに適用する圧縮のレベルを定義します。</span><span class="sxs-lookup"><span data-stu-id="b4775-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4775-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b4775-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4775-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="b4775-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="b4775-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b4775-108">Property set:</span></span>  <br/> |<span data-ttu-id="b4775-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b4775-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b4775-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b4775-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b4775-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="b4775-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="b4775-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b4775-112">Data type:</span></span>  <br/> |<span data-ttu-id="b4775-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b4775-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b4775-114">領域:</span><span class="sxs-lookup"><span data-stu-id="b4775-114">Area:</span></span>  <br/> |<span data-ttu-id="b4775-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="b4775-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4775-116">注釈</span><span class="sxs-lookup"><span data-stu-id="b4775-116">Remarks</span></span>

<span data-ttu-id="b4775-117">有効な圧縮レベルは、次のように。</span><span class="sxs-lookup"><span data-stu-id="b4775-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="b4775-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b4775-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4775-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b4775-119">Protocol specifications</span></span>

<span data-ttu-id="b4775-120">[MS OXPROPS]</span><span class="sxs-lookup"><span data-stu-id="b4775-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="b4775-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b4775-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4775-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b4775-122">Header files</span></span>

<span data-ttu-id="b4775-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4775-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4775-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b4775-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4775-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4775-125">See also</span></span>



[<span data-ttu-id="b4775-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b4775-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4775-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b4775-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4775-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b4775-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4775-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b4775-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

