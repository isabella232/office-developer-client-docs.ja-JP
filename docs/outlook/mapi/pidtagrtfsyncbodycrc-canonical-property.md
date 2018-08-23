---
title: PidTagRtfSyncBodyCrc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7c72b87eec6d0a14b0ebba10529ef5d898747028
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572978"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a><span data-ttu-id="f41fb-103">PidTagRtfSyncBodyCrc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f41fb-103">PidTagRtfSyncBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="f41fb-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f41fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f41fb-105">メッセージ テキストに計算された巡回冗長検査 (CRC) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f41fb-105">Contains the cyclical redundancy check (CRC) computed for the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f41fb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f41fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f41fb-107">PR_RTF_SYNC_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="f41fb-107">PR_RTF_SYNC_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="f41fb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f41fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f41fb-109">0x1006</span><span class="sxs-lookup"><span data-stu-id="f41fb-109">0x1006</span></span>  <br/> |
|<span data-ttu-id="f41fb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f41fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="f41fb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f41fb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f41fb-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f41fb-112">Area:</span></span>  <br/> |<span data-ttu-id="f41fb-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="f41fb-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f41fb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f41fb-114">Remarks</span></span>

<span data-ttu-id="f41fb-115">[](rtfsync.md)関数は、メッセージに重要と見なされる文字だけを使用して、CRC を計算します。</span><span class="sxs-lookup"><span data-stu-id="f41fb-115">The [RTFSync](rtfsync.md) function computes the CRC by using only the characters that it considers to be significant to the message.</span></span> <span data-ttu-id="f41fb-116">たとえば、いくつかの空白および他の無視可能な文字は、CRC から省略されます。</span><span class="sxs-lookup"><span data-stu-id="f41fb-116">For example, some white space and other ignorable characters are omitted from the CRC.</span></span> 
  
<span data-ttu-id="f41fb-117">このプロパティは、リッチ テキスト形式 (RTF) 補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="f41fb-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="f41fb-118">これらのプロパティ**へ**の関数で使用され、クライアント アプリケーションで直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="f41fb-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f41fb-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f41fb-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f41fb-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f41fb-120">Protocol specifications</span></span>

<span data-ttu-id="f41fb-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f41fb-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f41fb-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f41fb-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f41fb-123">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f41fb-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f41fb-124">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="f41fb-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f41fb-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f41fb-125">Header files</span></span>

<span data-ttu-id="f41fb-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f41fb-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f41fb-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f41fb-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f41fb-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f41fb-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f41fb-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f41fb-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f41fb-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="f41fb-130">See also</span></span>



[<span data-ttu-id="f41fb-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f41fb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f41fb-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f41fb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f41fb-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f41fb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f41fb-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f41fb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

