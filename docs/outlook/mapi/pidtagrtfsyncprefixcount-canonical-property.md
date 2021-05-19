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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 61683534504b7451f126591af149d11306cff1bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357863"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="c71ff-103">PidTagRtfSyncPrefixCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c71ff-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="c71ff-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c71ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c71ff-105">メッセージの重要な文字の前に表示される無視できる文字の数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c71ff-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c71ff-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c71ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c71ff-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="c71ff-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="c71ff-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c71ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c71ff-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="c71ff-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="c71ff-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c71ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="c71ff-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c71ff-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c71ff-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c71ff-112">Area:</span></span>  <br/> |<span data-ttu-id="c71ff-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="c71ff-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c71ff-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c71ff-114">Remarks</span></span>

<span data-ttu-id="c71ff-115">プレフィックス文字の数に空白は含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="c71ff-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="c71ff-116">このプロパティは、リッチ テキスト形式 (RTF) 補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="c71ff-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="c71ff-117">RTF 補助プロパティは [RTFSync](rtfsync.md) 関数で使用され、クライアント アプリケーションによって直接使用される意図はありません。</span><span class="sxs-lookup"><span data-stu-id="c71ff-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c71ff-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c71ff-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c71ff-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c71ff-119">Protocol specifications</span></span>

<span data-ttu-id="c71ff-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c71ff-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c71ff-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="c71ff-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c71ff-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c71ff-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c71ff-123">メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。</span><span class="sxs-lookup"><span data-stu-id="c71ff-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c71ff-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c71ff-124">Header files</span></span>

<span data-ttu-id="c71ff-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c71ff-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c71ff-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c71ff-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c71ff-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c71ff-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c71ff-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c71ff-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c71ff-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c71ff-129">See also</span></span>



[<span data-ttu-id="c71ff-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c71ff-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c71ff-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c71ff-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c71ff-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c71ff-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c71ff-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c71ff-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

