---
title: PidTagRuleProviderData 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e4d209c4f185ff253476beb04913e6a64884f9b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335421"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="05abe-103">PidTagRuleProviderData 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="05abe-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="05abe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05abe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05abe-105">クライアントがクライアントを排他的に使用するために設定する不透明なプロパティ。</span><span class="sxs-lookup"><span data-stu-id="05abe-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05abe-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="05abe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05abe-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="05abe-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="05abe-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="05abe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="05abe-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="05abe-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="05abe-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="05abe-110">Data type:</span></span>  <br/> |<span data-ttu-id="05abe-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="05abe-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="05abe-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="05abe-112">Area:</span></span>  <br/> |<span data-ttu-id="05abe-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="05abe-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05abe-114">注釈</span><span class="sxs-lookup"><span data-stu-id="05abe-114">Remarks</span></span>

<span data-ttu-id="05abe-115">サーバーは、クライアントが設定した場合は、このプロパティの値を保持する必要がありますが、ルールの評価と処理中に内容を無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05abe-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="05abe-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="05abe-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05abe-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="05abe-117">Protocol specifications</span></span>

<span data-ttu-id="05abe-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05abe-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05abe-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="05abe-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="05abe-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05abe-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05abe-121">サーバー上の受信メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="05abe-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05abe-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="05abe-122">Header files</span></span>

<span data-ttu-id="05abe-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05abe-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="05abe-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="05abe-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="05abe-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="05abe-125">Mapitags.h</span></span>
  
> <span data-ttu-id="05abe-126">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="05abe-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="05abe-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="05abe-127">See also</span></span>



[<span data-ttu-id="05abe-128">PidTagRuleProvider 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="05abe-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="05abe-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="05abe-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05abe-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="05abe-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05abe-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="05abe-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05abe-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="05abe-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

