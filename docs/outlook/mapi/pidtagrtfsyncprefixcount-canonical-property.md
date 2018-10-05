---
title: PidTagRtfSyncPrefixCount 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 61683534504b7451f126591af149d11306cff1bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389814"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="73cc4-103">PidTagRtfSyncPrefixCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="73cc4-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="73cc4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73cc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73cc4-105">メッセージの重要な文字の前に表示される無視可能な文字の数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="73cc4-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="73cc4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="73cc4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73cc4-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="73cc4-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="73cc4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="73cc4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="73cc4-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="73cc4-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="73cc4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="73cc4-110">Data type:</span></span>  <br/> |<span data-ttu-id="73cc4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="73cc4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="73cc4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="73cc4-112">Area:</span></span>  <br/> |<span data-ttu-id="73cc4-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="73cc4-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73cc4-114">備考</span><span class="sxs-lookup"><span data-stu-id="73cc4-114">Remarks</span></span>

<span data-ttu-id="73cc4-115">プレフィックス文字の数では、ホワイト スペースは含まれません。</span><span class="sxs-lookup"><span data-stu-id="73cc4-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="73cc4-116">このプロパティは、リッチ テキスト形式 (RTF) 補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="73cc4-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="73cc4-117">RTF の補助プロパティでは、[行う](rtfsync.md)関数によって使用され、クライアント アプリケーションで直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="73cc4-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="73cc4-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="73cc4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="73cc4-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="73cc4-119">Protocol specifications</span></span>

<span data-ttu-id="73cc4-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73cc4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73cc4-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="73cc4-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="73cc4-122">[[MS OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73cc4-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73cc4-123">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="73cc4-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="73cc4-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="73cc4-124">Header files</span></span>

<span data-ttu-id="73cc4-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73cc4-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="73cc4-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="73cc4-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="73cc4-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="73cc4-127">Mapitags.h</span></span>
  
> <span data-ttu-id="73cc4-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="73cc4-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73cc4-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="73cc4-129">See also</span></span>



[<span data-ttu-id="73cc4-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="73cc4-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73cc4-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="73cc4-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73cc4-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="73cc4-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73cc4-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="73cc4-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

