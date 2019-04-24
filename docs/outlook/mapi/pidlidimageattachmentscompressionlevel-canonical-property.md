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
ms.openlocfilehash: 8600cc7071fbe5c08d5df074f9bf59f4320b7f18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357583"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="27edf-103">PidLidImageAttachmentsCompressionLevel 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="27edf-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="27edf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27edf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27edf-105">画像の添付ファイルに適用する圧縮レベルを定義します。</span><span class="sxs-lookup"><span data-stu-id="27edf-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27edf-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="27edf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27edf-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="27edf-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="27edf-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="27edf-108">Property set:</span></span>  <br/> |<span data-ttu-id="27edf-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="27edf-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="27edf-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="27edf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="27edf-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="27edf-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="27edf-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="27edf-112">Data type:</span></span>  <br/> |<span data-ttu-id="27edf-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="27edf-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="27edf-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="27edf-114">Area:</span></span>  <br/> |<span data-ttu-id="27edf-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="27edf-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27edf-116">解説</span><span class="sxs-lookup"><span data-stu-id="27edf-116">Remarks</span></span>

<span data-ttu-id="27edf-117">有効な圧縮レベルは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="27edf-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="27edf-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="27edf-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27edf-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="27edf-119">Protocol specifications</span></span>

<span data-ttu-id="27edf-120">[[OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="27edf-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="27edf-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="27edf-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27edf-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="27edf-122">Header files</span></span>

<span data-ttu-id="27edf-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27edf-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="27edf-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="27edf-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27edf-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="27edf-125">See also</span></span>



[<span data-ttu-id="27edf-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="27edf-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27edf-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="27edf-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27edf-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="27edf-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27edf-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="27edf-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

