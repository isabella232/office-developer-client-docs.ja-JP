---
title: PidTagRtfSyncBodyCount 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f6e687412dfce1e5fcee6b4a4d64f3e5106455f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331256"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a><span data-ttu-id="6f16c-103">PidTagRtfSyncBodyCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6f16c-103">PidTagRtfSyncBodyCount Canonical Property</span></span>

  
  
<span data-ttu-id="6f16c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f16c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f16c-105">メッセージ テキストの重要な文字の数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f16c-105">Contains a count of the significant characters of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f16c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6f16c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f16c-107">PR_RTF_SYNC_BODY_COUNT</span><span class="sxs-lookup"><span data-stu-id="6f16c-107">PR_RTF_SYNC_BODY_COUNT</span></span>  <br/> |
|<span data-ttu-id="6f16c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6f16c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f16c-109">0x1007</span><span class="sxs-lookup"><span data-stu-id="6f16c-109">0x1007</span></span>  <br/> |
|<span data-ttu-id="6f16c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6f16c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f16c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6f16c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6f16c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="6f16c-112">Area:</span></span>  <br/> |<span data-ttu-id="6f16c-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="6f16c-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f16c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6f16c-114">Remarks</span></span>

<span data-ttu-id="6f16c-115">[RTFSync 関数](rtfsync.md)は、メッセージにとって重要と見なされる文字のみを使用して、テキスト内の文字数を計算します。</span><span class="sxs-lookup"><span data-stu-id="6f16c-115">The [RTFSync](rtfsync.md) function computes the count of characters in the text using only those that it considers to be significant to the message.</span></span> <span data-ttu-id="6f16c-116">たとえば、空白や他の無視できる文字はカウントから省略されます。</span><span class="sxs-lookup"><span data-stu-id="6f16c-116">For example, some white space and other ignorable characters are omitted from the count.</span></span> 
  
<span data-ttu-id="6f16c-117">このプロパティは、リッチ テキスト形式 (RTF) 補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="6f16c-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="6f16c-118">これらのプロパティは **RTFSync 関数で使用** され、クライアント アプリケーションによって直接使用される意図はありません。</span><span class="sxs-lookup"><span data-stu-id="6f16c-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6f16c-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6f16c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f16c-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6f16c-120">Protocol specifications</span></span>

<span data-ttu-id="6f16c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f16c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f16c-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="6f16c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6f16c-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f16c-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f16c-124">メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。</span><span class="sxs-lookup"><span data-stu-id="6f16c-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f16c-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6f16c-125">Header files</span></span>

<span data-ttu-id="6f16c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f16c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f16c-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6f16c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f16c-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6f16c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="6f16c-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="6f16c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f16c-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f16c-130">See also</span></span>



[<span data-ttu-id="6f16c-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6f16c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f16c-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6f16c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f16c-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="6f16c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f16c-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="6f16c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

