---
title: PidTagRtfSyncBodyCount の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 09274c21df3a93abc19aa8158da976e2d16f3e7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803407"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a><span data-ttu-id="b8051-103">PidTagRtfSyncBodyCount の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b8051-103">PidTagRtfSyncBodyCount Canonical Property</span></span>

  
  
<span data-ttu-id="b8051-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b8051-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b8051-105">重要なメッセージのテキストの文字数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b8051-105">Contains a count of the significant characters of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b8051-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b8051-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b8051-107">PR_RTF_SYNC_BODY_COUNT</span><span class="sxs-lookup"><span data-stu-id="b8051-107">PR_RTF_SYNC_BODY_COUNT</span></span>  <br/> |
|<span data-ttu-id="b8051-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b8051-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b8051-109">0x1007</span><span class="sxs-lookup"><span data-stu-id="b8051-109">0x1007</span></span>  <br/> |
|<span data-ttu-id="b8051-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="b8051-110">Data type:</span></span>  <br/> |<span data-ttu-id="b8051-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b8051-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b8051-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b8051-112">Area:</span></span>  <br/> |<span data-ttu-id="b8051-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="b8051-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8051-114">備考</span><span class="sxs-lookup"><span data-stu-id="b8051-114">Remarks</span></span>

<span data-ttu-id="b8051-115">[](rtfsync.md)関数は、メッセージに重要と見なされるものだけを使用してテキスト内の文字数を計算します。</span><span class="sxs-lookup"><span data-stu-id="b8051-115">The [RTFSync](rtfsync.md) function computes the count of characters in the text using only those that it considers to be significant to the message.</span></span> <span data-ttu-id="b8051-116">などのいくつかの空白および他の無視可能な文字はカウントから省略されます。</span><span class="sxs-lookup"><span data-stu-id="b8051-116">For example, some white space and other ignorable characters are omitted from the count.</span></span> 
  
<span data-ttu-id="b8051-117">このプロパティは、リッチ テキスト形式 (RTF) 補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="b8051-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="b8051-118">これらのプロパティ**へ**の関数で使用され、クライアント アプリケーションで直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="b8051-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b8051-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b8051-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b8051-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b8051-120">Protocol specifications</span></span>

<span data-ttu-id="b8051-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8051-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8051-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b8051-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b8051-123">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8051-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8051-124">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="b8051-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b8051-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b8051-125">Header files</span></span>

<span data-ttu-id="b8051-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b8051-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b8051-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b8051-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b8051-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b8051-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b8051-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b8051-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8051-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="b8051-130">See also</span></span>



[<span data-ttu-id="b8051-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8051-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b8051-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8051-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b8051-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="b8051-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b8051-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="b8051-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

