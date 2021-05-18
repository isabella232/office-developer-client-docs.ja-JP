---
title: PidTagRuleSequence 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleSequence
api_type:
- COM
ms.assetid: c42f2539-f7d6-464a-a82c-f0ac51823168
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 70e7a20a69b7467c1d8c31469273dcc28ce219ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321246"
---
# <a name="pidtagrulesequence-canonical-property"></a><span data-ttu-id="06a33-103">PidTagRuleSequence 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="06a33-103">PidTagRuleSequence Canonical Property</span></span>

  
  
<span data-ttu-id="06a33-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06a33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06a33-105">ルールが評価および実行される順序を決定するために使用される値。</span><span class="sxs-lookup"><span data-stu-id="06a33-105">A value used to determine the order in which rules are evaluated and executed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06a33-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="06a33-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06a33-107">PR_RULE_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="06a33-107">PR_RULE_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="06a33-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="06a33-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06a33-109">0x6676</span><span class="sxs-lookup"><span data-stu-id="06a33-109">0x6676</span></span>  <br/> |
|<span data-ttu-id="06a33-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="06a33-110">Data type:</span></span>  <br/> |<span data-ttu-id="06a33-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="06a33-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="06a33-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="06a33-112">Area:</span></span>  <br/> |<span data-ttu-id="06a33-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="06a33-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06a33-114">注釈</span><span class="sxs-lookup"><span data-stu-id="06a33-114">Remarks</span></span>

<span data-ttu-id="06a33-115">ルールは、この値の増加順序に従って順番に評価されます。</span><span class="sxs-lookup"><span data-stu-id="06a33-115">Rules are evaluated in sequence according to the increasing order of this value.</span></span> <span data-ttu-id="06a33-116">このプロパティで同じ値を持つルールの評価順序は未定義です。</span><span class="sxs-lookup"><span data-stu-id="06a33-116">The evaluation order for rules that have the same value in this property is undefined.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="06a33-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="06a33-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="06a33-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="06a33-118">Protocol specifications</span></span>

<span data-ttu-id="06a33-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06a33-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06a33-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="06a33-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="06a33-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06a33-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06a33-122">サーバー上の受信メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="06a33-122">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="06a33-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06a33-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06a33-124">メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーに代わって動作するメッセージアイテムと予定表アイテムとのやり取りを指定します。</span><span class="sxs-lookup"><span data-stu-id="06a33-124">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="06a33-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06a33-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06a33-126">コア テーブル オブジェクトに対して許容される操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="06a33-126">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="06a33-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06a33-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06a33-128">コア メッセージ ストア オブジェクトに対して許容される操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="06a33-128">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="06a33-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="06a33-129">Header files</span></span>

<span data-ttu-id="06a33-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06a33-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="06a33-131">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="06a33-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="06a33-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06a33-132">Mapitags.h</span></span>
  
> <span data-ttu-id="06a33-133">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="06a33-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06a33-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="06a33-134">See also</span></span>



[<span data-ttu-id="06a33-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="06a33-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06a33-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="06a33-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06a33-137">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="06a33-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06a33-138">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="06a33-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

