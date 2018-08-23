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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 29579f91a85e74b568610c749d9408f813f157f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803442"
---
# <a name="pidtagrulesequence-canonical-property"></a><span data-ttu-id="94617-103">PidTagRuleSequence 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94617-103">PidTagRuleSequence Canonical Property</span></span>

  
  
<span data-ttu-id="94617-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="94617-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="94617-105">ルールを評価および実行の順序を決定するために使用する値です。</span><span class="sxs-lookup"><span data-stu-id="94617-105">A value used to determine the order in which rules are evaluated and executed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94617-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="94617-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94617-107">PR_RULE_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="94617-107">PR_RULE_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="94617-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="94617-108">Identifier:</span></span>  <br/> |<span data-ttu-id="94617-109">0x6676</span><span class="sxs-lookup"><span data-stu-id="94617-109">0x6676</span></span>  <br/> |
|<span data-ttu-id="94617-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="94617-110">Data type:</span></span>  <br/> |<span data-ttu-id="94617-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="94617-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="94617-112">領域:</span><span class="sxs-lookup"><span data-stu-id="94617-112">Area:</span></span>  <br/> |<span data-ttu-id="94617-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="94617-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94617-114">注釈</span><span class="sxs-lookup"><span data-stu-id="94617-114">Remarks</span></span>

<span data-ttu-id="94617-115">によってこの値の昇順のシーケンスでは、ルールが評価されます。</span><span class="sxs-lookup"><span data-stu-id="94617-115">Rules are evaluated in sequence according to the increasing order of this value.</span></span> <span data-ttu-id="94617-116">このプロパティに同じ値を設定するルールの評価順序は定義されていません。</span><span class="sxs-lookup"><span data-stu-id="94617-116">The evaluation order for rules that have the same value in this property is undefined.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="94617-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="94617-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94617-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="94617-118">Protocol specifications</span></span>

<span data-ttu-id="94617-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94617-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94617-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="94617-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="94617-121">[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94617-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94617-122">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="94617-122">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="94617-123">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94617-123">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94617-124">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のアイテムとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="94617-124">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="94617-125">[[MS OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94617-125">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94617-126">テーブルのコア オブジェクトに許容される操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="94617-126">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="94617-127">[[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94617-127">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94617-128">コア メッセージのストア オブジェクトの許可された操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="94617-128">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94617-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="94617-129">Header files</span></span>

<span data-ttu-id="94617-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94617-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="94617-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="94617-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="94617-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="94617-132">Mapitags.h</span></span>
  
> <span data-ttu-id="94617-133">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="94617-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94617-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="94617-134">See also</span></span>



[<span data-ttu-id="94617-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="94617-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94617-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="94617-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94617-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="94617-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94617-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="94617-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

