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
ms.openlocfilehash: 24ef1d4e3e936426aea8216119e8ada9f6122e95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331179"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a><span data-ttu-id="67ed0-103">PidTagRtfSyncBodyTag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="67ed0-103">PidTagRtfSyncBodyTag Canonical Property</span></span>

  
  
<span data-ttu-id="67ed0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67ed0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67ed0-105">メッセージテキストの先頭に表示される重要な文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="67ed0-105">Contains significant characters that appear at the beginning of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="67ed0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="67ed0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67ed0-107">PR_RTF_SYNC_BODY_TAG、PR_RTF_SYNC_BODY_TAG_A、PR_RTF_SYNC_BODY_TAG_W</span><span class="sxs-lookup"><span data-stu-id="67ed0-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span></span>  <br/> |
|<span data-ttu-id="67ed0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="67ed0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67ed0-109">0x1008</span><span class="sxs-lookup"><span data-stu-id="67ed0-109">0x1008</span></span>  <br/> |
|<span data-ttu-id="67ed0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="67ed0-110">Data type:</span></span>  <br/> |<span data-ttu-id="67ed0-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="67ed0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="67ed0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="67ed0-112">Area:</span></span>  <br/> |<span data-ttu-id="67ed0-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="67ed0-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67ed0-114">解説</span><span class="sxs-lookup"><span data-stu-id="67ed0-114">Remarks</span></span>

<span data-ttu-id="67ed0-115">[rtfsync](rtfsync.md)関数は、テキストタグを使用して、メッセージテキストの先頭を示します。</span><span class="sxs-lookup"><span data-stu-id="67ed0-115">The [RTFSync](rtfsync.md) function uses the text tag to indicate the beginning of the message text.</span></span> <span data-ttu-id="67ed0-116">テキストが変更されると、タグは前のテキストの先頭を検索するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="67ed0-116">When the text is modified, the tag is used to find the beginning of the previous text.</span></span> 
  
<span data-ttu-id="67ed0-117">これらのプロパティは、リッチテキスト形式の補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="67ed0-117">These properties are Rich Text Format auxiliary properties.</span></span> <span data-ttu-id="67ed0-118">これらは、 **rtfsync**関数で使用され、クライアントアプリケーションによって直接使用されることを意図したものではありません。</span><span class="sxs-lookup"><span data-stu-id="67ed0-118">They are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="67ed0-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="67ed0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67ed0-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="67ed0-120">Protocol specifications</span></span>

<span data-ttu-id="67ed0-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67ed0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67ed0-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="67ed0-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="67ed0-123">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67ed0-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67ed0-124">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="67ed0-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67ed0-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="67ed0-125">Header files</span></span>

<span data-ttu-id="67ed0-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67ed0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="67ed0-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="67ed0-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="67ed0-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="67ed0-128">Mapitags.h</span></span>
  
> <span data-ttu-id="67ed0-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="67ed0-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67ed0-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="67ed0-130">See also</span></span>



[<span data-ttu-id="67ed0-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="67ed0-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67ed0-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="67ed0-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67ed0-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="67ed0-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67ed0-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="67ed0-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

