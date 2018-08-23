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
ms.openlocfilehash: 55b965374bb1d7e5859f0cac5cc2f61956ea5b55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578921"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="5ea02-103">PidLidImageAttachmentsCompressionLevel 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5ea02-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="5ea02-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ea02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ea02-105">画像添付ファイルに適用する圧縮のレベルを定義します。</span><span class="sxs-lookup"><span data-stu-id="5ea02-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ea02-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5ea02-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ea02-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="5ea02-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="5ea02-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ea02-108">Property set:</span></span>  <br/> |<span data-ttu-id="5ea02-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5ea02-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5ea02-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5ea02-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5ea02-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="5ea02-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="5ea02-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5ea02-112">Data type:</span></span>  <br/> |<span data-ttu-id="5ea02-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5ea02-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5ea02-114">領域:</span><span class="sxs-lookup"><span data-stu-id="5ea02-114">Area:</span></span>  <br/> |<span data-ttu-id="5ea02-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="5ea02-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ea02-116">注釈</span><span class="sxs-lookup"><span data-stu-id="5ea02-116">Remarks</span></span>

<span data-ttu-id="5ea02-117">有効な圧縮レベルは、次のように。</span><span class="sxs-lookup"><span data-stu-id="5ea02-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="5ea02-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5ea02-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5ea02-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5ea02-119">Protocol specifications</span></span>

<span data-ttu-id="5ea02-120">[MS OXPROPS]</span><span class="sxs-lookup"><span data-stu-id="5ea02-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="5ea02-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5ea02-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5ea02-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5ea02-122">Header files</span></span>

<span data-ttu-id="5ea02-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ea02-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ea02-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5ea02-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ea02-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ea02-125">See also</span></span>



[<span data-ttu-id="5ea02-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5ea02-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ea02-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5ea02-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ea02-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5ea02-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ea02-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5ea02-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

