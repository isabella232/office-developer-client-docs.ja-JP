---
title: PidTagRtfSyncTrailingCount 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7efa8dccf4c2c6da0ad60688d06d241d336e3943
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581007"
---
# <a name="pidtagrtfsynctrailingcount-canonical-property"></a><span data-ttu-id="4a31d-103">PidTagRtfSyncTrailingCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a31d-103">PidTagRtfSyncTrailingCount Canonical Property</span></span>

  
  
<span data-ttu-id="4a31d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a31d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a31d-105">メッセージの重要な文字の後に表示される、無視できる文字の数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4a31d-105">Contains a count of the ignorable characters that appear after the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a31d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4a31d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a31d-107">PR_RTF_SYNC_TRAILING_COUNT</span><span class="sxs-lookup"><span data-stu-id="4a31d-107">PR_RTF_SYNC_TRAILING_COUNT</span></span>  <br/> |
|<span data-ttu-id="4a31d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4a31d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a31d-109">0x1011</span><span class="sxs-lookup"><span data-stu-id="4a31d-109">0x1011</span></span>  <br/> |
|<span data-ttu-id="4a31d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4a31d-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a31d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4a31d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4a31d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4a31d-112">Area:</span></span>  <br/> |<span data-ttu-id="4a31d-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="4a31d-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a31d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4a31d-114">Remarks</span></span>

<span data-ttu-id="4a31d-115">このプロパティは、リッチ テキスト形式 (RFT) 補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="4a31d-115">This property is a Rich Text Format (RFT) auxiliary property.</span></span> <span data-ttu-id="4a31d-116">これらのプロパティ[へ](rtfsync.md)の関数で使用され、クライアント アプリケーションで直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="4a31d-116">These properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4a31d-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4a31d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a31d-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4a31d-118">Protocol specifications</span></span>

<span data-ttu-id="4a31d-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a31d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a31d-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4a31d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a31d-121">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a31d-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a31d-122">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="4a31d-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a31d-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4a31d-123">Header files</span></span>

<span data-ttu-id="4a31d-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a31d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a31d-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4a31d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a31d-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4a31d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4a31d-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4a31d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a31d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="4a31d-128">See also</span></span>



[<span data-ttu-id="4a31d-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a31d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a31d-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a31d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a31d-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4a31d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a31d-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4a31d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

