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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8600cc7071fbe5c08d5df074f9bf59f4320b7f18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413830"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="f6b2d-103">PidLidImageAttachmentsCompressionLevel 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f6b2d-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="f6b2d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6b2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6b2d-105">イメージ添付ファイルに適用する圧縮レベルを定義します。</span><span class="sxs-lookup"><span data-stu-id="f6b2d-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6b2d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f6b2d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6b2d-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="f6b2d-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="f6b2d-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="f6b2d-108">Property set:</span></span>  <br/> |<span data-ttu-id="f6b2d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f6b2d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f6b2d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f6b2d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f6b2d-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="f6b2d-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="f6b2d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f6b2d-112">Data type:</span></span>  <br/> |<span data-ttu-id="f6b2d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f6b2d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f6b2d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="f6b2d-114">Area:</span></span>  <br/> |<span data-ttu-id="f6b2d-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="f6b2d-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6b2d-116">注釈</span><span class="sxs-lookup"><span data-stu-id="f6b2d-116">Remarks</span></span>

<span data-ttu-id="f6b2d-117">有効な圧縮レベルは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f6b2d-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="f6b2d-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f6b2d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f6b2d-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f6b2d-119">Protocol specifications</span></span>

<span data-ttu-id="f6b2d-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="f6b2d-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="f6b2d-121">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="f6b2d-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f6b2d-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f6b2d-122">Header files</span></span>

<span data-ttu-id="f6b2d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6b2d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6b2d-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f6b2d-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6b2d-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6b2d-125">See also</span></span>



[<span data-ttu-id="f6b2d-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f6b2d-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6b2d-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f6b2d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6b2d-128">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f6b2d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6b2d-129">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f6b2d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

