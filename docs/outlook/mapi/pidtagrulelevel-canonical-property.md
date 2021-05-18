---
title: PidTagRuleLevel 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleLevel
api_type:
- COM
ms.assetid: b1a30543-250d-4afb-87f2-448d90ee7cf9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3de5093f1fa395b1fba061f88a9b67b5dedf4740
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359529"
---
# <a name="pidtagrulelevel-canonical-property"></a><span data-ttu-id="ee52a-103">PidTagRuleLevel 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ee52a-103">PidTagRuleLevel Canonical Property</span></span>

  
  
<span data-ttu-id="ee52a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee52a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee52a-105">ルールの終了レベルを含む。</span><span class="sxs-lookup"><span data-stu-id="ee52a-105">Contains the exit level of a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee52a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ee52a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee52a-107">PR_RULE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="ee52a-107">PR_RULE_LEVEL</span></span>  <br/> |
|<span data-ttu-id="ee52a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ee52a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee52a-109">0x6683</span><span class="sxs-lookup"><span data-stu-id="ee52a-109">0x6683</span></span>  <br/> |
|<span data-ttu-id="ee52a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ee52a-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee52a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ee52a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ee52a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ee52a-112">Area:</span></span>  <br/> |<span data-ttu-id="ee52a-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="ee52a-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee52a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ee52a-114">Remarks</span></span>

<span data-ttu-id="ee52a-115">このプロパティを設定する場合、クライアントはクライアントに渡す0x00000000。</span><span class="sxs-lookup"><span data-stu-id="ee52a-115">If setting this property, the client must pass in 0x00000000.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ee52a-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ee52a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ee52a-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ee52a-117">Protocol specifications</span></span>

<span data-ttu-id="ee52a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee52a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee52a-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="ee52a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ee52a-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee52a-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee52a-121">メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーに代わって動作するメッセージアイテムと予定表アイテムとのやり取りを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee52a-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="ee52a-122">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee52a-122">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee52a-123">サーバー上の受信メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="ee52a-123">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ee52a-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ee52a-124">Header files</span></span>

<span data-ttu-id="ee52a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee52a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee52a-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ee52a-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ee52a-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ee52a-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ee52a-128">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="ee52a-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee52a-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee52a-129">See also</span></span>



[<span data-ttu-id="ee52a-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee52a-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="ee52a-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ee52a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee52a-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ee52a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee52a-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ee52a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee52a-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ee52a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

