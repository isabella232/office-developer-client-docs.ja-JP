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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 24ef1d4e3e936426aea8216119e8ada9f6122e95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331179"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a><span data-ttu-id="5e27e-103">PidTagRtfSyncBodyTag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e27e-103">PidTagRtfSyncBodyTag Canonical Property</span></span>

  
  
<span data-ttu-id="5e27e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e27e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e27e-105">メッセージ テキストの先頭に表示される重要な文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5e27e-105">Contains significant characters that appear at the beginning of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e27e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5e27e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e27e-107">PR_RTF_SYNC_BODY_TAG、PR_RTF_SYNC_BODY_TAG_A、PR_RTF_SYNC_BODY_TAG_W</span><span class="sxs-lookup"><span data-stu-id="5e27e-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span></span>  <br/> |
|<span data-ttu-id="5e27e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5e27e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e27e-109">0x1008</span><span class="sxs-lookup"><span data-stu-id="5e27e-109">0x1008</span></span>  <br/> |
|<span data-ttu-id="5e27e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5e27e-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e27e-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5e27e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5e27e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5e27e-112">Area:</span></span>  <br/> |<span data-ttu-id="5e27e-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="5e27e-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e27e-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5e27e-114">Remarks</span></span>

<span data-ttu-id="5e27e-115">[RTFSync 関数は](rtfsync.md)、テキスト タグを使用してメッセージ テキストの先頭を示します。</span><span class="sxs-lookup"><span data-stu-id="5e27e-115">The [RTFSync](rtfsync.md) function uses the text tag to indicate the beginning of the message text.</span></span> <span data-ttu-id="5e27e-116">テキストを変更すると、タグを使用して前のテキストの先頭を検索します。</span><span class="sxs-lookup"><span data-stu-id="5e27e-116">When the text is modified, the tag is used to find the beginning of the previous text.</span></span> 
  
<span data-ttu-id="5e27e-117">これらのプロパティは、リッチ テキスト形式の補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="5e27e-117">These properties are Rich Text Format auxiliary properties.</span></span> <span data-ttu-id="5e27e-118">これらは **RTFSync 関数によって使用** され、クライアント アプリケーションによって直接使用される意図はありません。</span><span class="sxs-lookup"><span data-stu-id="5e27e-118">They are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5e27e-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5e27e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e27e-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5e27e-120">Protocol specifications</span></span>

<span data-ttu-id="5e27e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e27e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e27e-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="5e27e-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5e27e-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e27e-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e27e-124">メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。</span><span class="sxs-lookup"><span data-stu-id="5e27e-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e27e-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5e27e-125">Header files</span></span>

<span data-ttu-id="5e27e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e27e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e27e-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5e27e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e27e-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5e27e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="5e27e-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="5e27e-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e27e-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e27e-130">See also</span></span>



[<span data-ttu-id="5e27e-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5e27e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e27e-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e27e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e27e-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5e27e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e27e-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5e27e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

