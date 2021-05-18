---
title: PidTagRuleProvider 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280606"
---
# <a name="pidtagruleprovider-canonical-property"></a><span data-ttu-id="695a8-103">PidTagRuleProvider 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="695a8-103">PidTagRuleProvider Canonical Property</span></span>

  
  
<span data-ttu-id="695a8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="695a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="695a8-105">ルールを設定するアプリケーションの名前を含む。</span><span class="sxs-lookup"><span data-stu-id="695a8-105">Contains the name of the application that sets a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="695a8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="695a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="695a8-107">PR_RULE_PROVIDER、PR_RULE_PROVIDER_A、PR_RULE_PROVIDER_W</span><span class="sxs-lookup"><span data-stu-id="695a8-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span></span>  <br/> |
|<span data-ttu-id="695a8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="695a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="695a8-109">0x6681</span><span class="sxs-lookup"><span data-stu-id="695a8-109">0x6681</span></span>  <br/> |
|<span data-ttu-id="695a8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="695a8-110">Data type:</span></span>  <br/> |<span data-ttu-id="695a8-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="695a8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="695a8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="695a8-112">Area:</span></span>  <br/> |<span data-ttu-id="695a8-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="695a8-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="695a8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="695a8-114">Remarks</span></span>

<span data-ttu-id="695a8-115">遅延アクションでは、ルール アクションを解釈して実行する必要があるコードを識別するために、これらのプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="695a8-115">Deferred actions need these properties to identify the code that must interpret and execute the rule action.</span></span>
  
<span data-ttu-id="695a8-116">メールボックスとフォルダーに格納されているルールは、ルール プロバイダー文字列によってそれらを所有するアプリケーションに関連付けられる。</span><span class="sxs-lookup"><span data-stu-id="695a8-116">Rules stored on mailboxes and folders are associated with the application that owns them by a rule provider string.</span></span> <span data-ttu-id="695a8-117">ルール プロバイダーは、ルール テーブル内のルールを設定および処理します。</span><span class="sxs-lookup"><span data-stu-id="695a8-117">A rule provider sets and handles rules in a rule table.</span></span> <span data-ttu-id="695a8-118">また、そのようなルールが設定されている場合に遅延アクションを処理する手段も提供します。</span><span class="sxs-lookup"><span data-stu-id="695a8-118">It also provides a means of handling any deferred actions if such rules are set.</span></span> <span data-ttu-id="695a8-119">遅延アクションは、情報ストアによって暗黙的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="695a8-119">Deferred actions are created implicitly by the information store.</span></span> <span data-ttu-id="695a8-120">別のストアへの移動またはコピー操作の場合、プロバイダーが遅延アクション ルールを設定する場合は、ルールが発生し、遅延アクションが作成された場合にアクションを実行するためのハンドラーを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="695a8-120">For move or copy operations to a different store, if a provider sets a deferred action rule, it must provide a handler to perform the action when the rule is fired and a deferred action is created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="695a8-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="695a8-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="695a8-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="695a8-122">Protocol specifications</span></span>

<span data-ttu-id="695a8-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="695a8-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="695a8-124">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="695a8-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="695a8-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="695a8-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="695a8-126">サーバー上の受信メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="695a8-126">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="695a8-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="695a8-127">Header files</span></span>

<span data-ttu-id="695a8-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="695a8-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="695a8-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="695a8-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="695a8-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="695a8-130">Mapitags.h</span></span>
  
> <span data-ttu-id="695a8-131">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="695a8-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="695a8-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="695a8-132">See also</span></span>



[<span data-ttu-id="695a8-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="695a8-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="695a8-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="695a8-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="695a8-135">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="695a8-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="695a8-136">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="695a8-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

