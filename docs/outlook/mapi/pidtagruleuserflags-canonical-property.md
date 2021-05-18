---
title: PidTagRuleUserFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleUserFlags
api_type:
- COM
ms.assetid: c5dfb21f-b35e-4521-bf2b-e3d03d98d75d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 235efce341e1870f0c33917f1c6d42b021727308
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321344"
---
# <a name="pidtagruleuserflags-canonical-property"></a><span data-ttu-id="9f436-103">PidTagRuleUserFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9f436-103">PidTagRuleUserFlags Canonical Property</span></span>

  
  
<span data-ttu-id="9f436-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f436-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f436-105">このプロパティは、クライアントの排他的な使用のためにクライアントによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="9f436-105">This property is set by the client for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f436-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9f436-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f436-107">PR_RULE_USER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="9f436-107">PR_RULE_USER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="9f436-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9f436-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9f436-109">0x6678</span><span class="sxs-lookup"><span data-stu-id="9f436-109">0x6678</span></span>  <br/> |
|<span data-ttu-id="9f436-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9f436-110">Data type:</span></span>  <br/> |<span data-ttu-id="9f436-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9f436-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9f436-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9f436-112">Area:</span></span>  <br/> |<span data-ttu-id="9f436-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="9f436-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f436-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9f436-114">Remarks</span></span>

<span data-ttu-id="9f436-115">このプロパティがクライアントによって設定されている場合、サーバーは、このプロパティの値を保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f436-115">The server must preserve the value of this property if it was set by the client.</span></span> <span data-ttu-id="9f436-116">サーバーは、ルールの評価と処理中に無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f436-116">The server must ignore it during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9f436-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9f436-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9f436-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9f436-118">Protocol specifications</span></span>

<span data-ttu-id="9f436-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f436-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f436-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="9f436-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9f436-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f436-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f436-122">サーバー上の受信メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="9f436-122">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9f436-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9f436-123">Header files</span></span>

<span data-ttu-id="9f436-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f436-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f436-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9f436-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9f436-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9f436-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9f436-127">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="9f436-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f436-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9f436-128">See also</span></span>



[<span data-ttu-id="9f436-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9f436-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f436-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9f436-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f436-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9f436-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f436-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9f436-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

