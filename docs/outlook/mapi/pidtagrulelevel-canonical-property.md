---
title: PidTagRuleLevel の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 55627161010996d59cf495845e73515da2a75fcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803412"
---
# <a name="pidtagrulelevel-canonical-property"></a><span data-ttu-id="79845-103">PidTagRuleLevel の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="79845-103">PidTagRuleLevel Canonical Property</span></span>

  
  
<span data-ttu-id="79845-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="79845-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="79845-105">規則の終了時のレベルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="79845-105">Contains the exit level of a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="79845-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="79845-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="79845-107">PR_RULE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="79845-107">PR_RULE_LEVEL</span></span>  <br/> |
|<span data-ttu-id="79845-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="79845-108">Identifier:</span></span>  <br/> |<span data-ttu-id="79845-109">0x6683</span><span class="sxs-lookup"><span data-stu-id="79845-109">0x6683</span></span>  <br/> |
|<span data-ttu-id="79845-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="79845-110">Data type:</span></span>  <br/> |<span data-ttu-id="79845-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="79845-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="79845-112">領域:</span><span class="sxs-lookup"><span data-stu-id="79845-112">Area:</span></span>  <br/> |<span data-ttu-id="79845-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="79845-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79845-114">備考</span><span class="sxs-lookup"><span data-stu-id="79845-114">Remarks</span></span>

<span data-ttu-id="79845-115">このプロパティを設定する場合、クライアントは 0x00000000 に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="79845-115">If setting this property, the client must pass in 0x00000000.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="79845-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="79845-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="79845-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="79845-117">Protocol specifications</span></span>

<span data-ttu-id="79845-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79845-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79845-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="79845-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="79845-120">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79845-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79845-121">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のアイテムとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="79845-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="79845-122">[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79845-122">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79845-123">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="79845-123">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="79845-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="79845-124">Header files</span></span>

<span data-ttu-id="79845-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="79845-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="79845-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="79845-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="79845-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="79845-127">Mapitags.h</span></span>
  
> <span data-ttu-id="79845-128">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="79845-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79845-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="79845-129">See also</span></span>



[<span data-ttu-id="79845-130">IExchangeModifyTable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="79845-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="79845-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="79845-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="79845-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="79845-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="79845-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="79845-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="79845-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="79845-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

