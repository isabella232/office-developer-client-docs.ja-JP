---
title: PidTagRtfSyncBodyTag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyTag
api_type:
- COM
ms.assetid: 2dab5018-4214-4162-93bc-e5565f3ac24c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bad754d21652d3f5278a6dad3ec06f4a0b533036
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803401"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a><span data-ttu-id="e6af7-103">PidTagRtfSyncBodyTag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e6af7-103">PidTagRtfSyncBodyTag Canonical Property</span></span>

  
  
<span data-ttu-id="e6af7-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6af7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6af7-105">メッセージ テキストの先頭に表示される重要な文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e6af7-105">Contains significant characters that appear at the beginning of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6af7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e6af7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e6af7-107">PR_RTF_SYNC_BODY_TAG、PR_RTF_SYNC_BODY_TAG_A、PR_RTF_SYNC_BODY_TAG_W</span><span class="sxs-lookup"><span data-stu-id="e6af7-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span></span>  <br/> |
|<span data-ttu-id="e6af7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e6af7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e6af7-109">0x1008</span><span class="sxs-lookup"><span data-stu-id="e6af7-109">0x1008</span></span>  <br/> |
|<span data-ttu-id="e6af7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e6af7-110">Data type:</span></span>  <br/> |<span data-ttu-id="e6af7-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e6af7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e6af7-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e6af7-112">Area:</span></span>  <br/> |<span data-ttu-id="e6af7-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="e6af7-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6af7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e6af7-114">Remarks</span></span>

<span data-ttu-id="e6af7-115">[](rtfsync.md)関数は、メッセージ テキストの先頭を示すために、テキストのタグを使用します。</span><span class="sxs-lookup"><span data-stu-id="e6af7-115">The [RTFSync](rtfsync.md) function uses the text tag to indicate the beginning of the message text.</span></span> <span data-ttu-id="e6af7-116">テキストが変更されると、前のテキストの先頭を検索するタグを使用します。</span><span class="sxs-lookup"><span data-stu-id="e6af7-116">When the text is modified, the tag is used to find the beginning of the previous text.</span></span> 
  
<span data-ttu-id="e6af7-117">これらのプロパティは、リッチ テキスト形式の補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="e6af7-117">These properties are Rich Text Format auxiliary properties.</span></span> <span data-ttu-id="e6af7-118">**** 関数で使用されて、クライアント アプリケーションで直接使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="e6af7-118">They are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e6af7-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e6af7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e6af7-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e6af7-120">Protocol specifications</span></span>

<span data-ttu-id="e6af7-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6af7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6af7-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e6af7-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e6af7-123">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6af7-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6af7-124">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="e6af7-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e6af7-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e6af7-125">Header files</span></span>

<span data-ttu-id="e6af7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6af7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e6af7-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e6af7-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e6af7-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e6af7-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e6af7-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e6af7-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e6af7-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="e6af7-130">See also</span></span>



[<span data-ttu-id="e6af7-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e6af7-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e6af7-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e6af7-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e6af7-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e6af7-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e6af7-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e6af7-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

