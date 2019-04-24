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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357863"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="d1876-103">PidTagRtfSyncPrefixCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d1876-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="d1876-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1876-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1876-105">メッセージの重要な文字の前に表示される無視できる文字の数を含みます。</span><span class="sxs-lookup"><span data-stu-id="d1876-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1876-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d1876-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1876-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="d1876-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="d1876-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d1876-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d1876-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="d1876-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="d1876-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d1876-110">Data type:</span></span>  <br/> |<span data-ttu-id="d1876-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d1876-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d1876-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d1876-112">Area:</span></span>  <br/> |<span data-ttu-id="d1876-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="d1876-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1876-114">解説</span><span class="sxs-lookup"><span data-stu-id="d1876-114">Remarks</span></span>

<span data-ttu-id="d1876-115">先頭文字の数にスペースは含まれません。</span><span class="sxs-lookup"><span data-stu-id="d1876-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="d1876-116">このプロパティは、リッチテキスト形式 (RTF) の補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="d1876-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="d1876-117">RTF 補助プロパティは、 [rtfsync](rtfsync.md)関数で使用され、クライアントアプリケーションによって直接使用されることを意図したものではありません。</span><span class="sxs-lookup"><span data-stu-id="d1876-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d1876-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d1876-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1876-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d1876-119">Protocol specifications</span></span>

<span data-ttu-id="d1876-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1876-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1876-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d1876-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d1876-122">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1876-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1876-123">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="d1876-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1876-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="d1876-124">Header files</span></span>

<span data-ttu-id="d1876-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1876-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1876-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d1876-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d1876-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="d1876-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d1876-128">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1876-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1876-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1876-129">See also</span></span>



[<span data-ttu-id="d1876-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d1876-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1876-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d1876-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1876-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d1876-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1876-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d1876-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

