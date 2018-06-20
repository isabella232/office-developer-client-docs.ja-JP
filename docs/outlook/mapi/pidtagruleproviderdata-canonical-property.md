---
title: PidTagRuleProviderData の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 054299e6bdf685163bc23678a2070f5d702a4529
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803423"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="edb27-103">PidTagRuleProviderData の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="edb27-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="edb27-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="edb27-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="edb27-105">クライアントの設定は、クライアントが排他的に使用する不透明なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="edb27-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="edb27-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="edb27-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="edb27-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="edb27-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="edb27-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="edb27-108">Identifier:</span></span>  <br/> |<span data-ttu-id="edb27-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="edb27-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="edb27-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="edb27-110">Data type:</span></span>  <br/> |<span data-ttu-id="edb27-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="edb27-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="edb27-112">領域:</span><span class="sxs-lookup"><span data-stu-id="edb27-112">Area:</span></span>  <br/> |<span data-ttu-id="edb27-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="edb27-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edb27-114">備考</span><span class="sxs-lookup"><span data-stu-id="edb27-114">Remarks</span></span>

<span data-ttu-id="edb27-115">サーバーは、クライアントが設定されている場合、このプロパティの値を保持する必要がありますが、ルールの評価および処理中にその内容を無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="edb27-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="edb27-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="edb27-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="edb27-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="edb27-117">Protocol specifications</span></span>

<span data-ttu-id="edb27-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edb27-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edb27-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="edb27-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="edb27-120">[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edb27-120">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edb27-121">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="edb27-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="edb27-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="edb27-122">Header files</span></span>

<span data-ttu-id="edb27-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edb27-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="edb27-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="edb27-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="edb27-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="edb27-125">Mapitags.h</span></span>
  
> <span data-ttu-id="edb27-126">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="edb27-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="edb27-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="edb27-127">See also</span></span>



[<span data-ttu-id="edb27-128">PidTagRuleProvider の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="edb27-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="edb27-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="edb27-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edb27-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="edb27-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edb27-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="edb27-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edb27-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="edb27-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

