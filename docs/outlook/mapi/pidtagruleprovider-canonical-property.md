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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385978"
---
# <a name="pidtagruleprovider-canonical-property"></a><span data-ttu-id="3777c-103">PidTagRuleProvider 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3777c-103">PidTagRuleProvider Canonical Property</span></span>

  
  
<span data-ttu-id="3777c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3777c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3777c-105">ルールを設定するアプリケーションの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3777c-105">Contains the name of the application that sets a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3777c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3777c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3777c-107">PR_RULE_PROVIDER、PR_RULE_PROVIDER_A、PR_RULE_PROVIDER_W</span><span class="sxs-lookup"><span data-stu-id="3777c-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span></span>  <br/> |
|<span data-ttu-id="3777c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3777c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3777c-109">0x6681</span><span class="sxs-lookup"><span data-stu-id="3777c-109">0x6681</span></span>  <br/> |
|<span data-ttu-id="3777c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3777c-110">Data type:</span></span>  <br/> |<span data-ttu-id="3777c-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3777c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3777c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3777c-112">Area:</span></span>  <br/> |<span data-ttu-id="3777c-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="3777c-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3777c-114">備考</span><span class="sxs-lookup"><span data-stu-id="3777c-114">Remarks</span></span>

<span data-ttu-id="3777c-115">これらのコードを識別するプロパティを解釈し、規則の操作を実行する必要がありますアクションの必要性を延期します。</span><span class="sxs-lookup"><span data-stu-id="3777c-115">Deferred actions need these properties to identify the code that must interpret and execute the rule action.</span></span>
  
<span data-ttu-id="3777c-116">メールボックスおよびフォルダーに格納されているルールは、ルールのプロバイダー文字列でそれらを所有するアプリケーションに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="3777c-116">Rules stored on mailboxes and folders are associated with the application that owns them by a rule provider string.</span></span> <span data-ttu-id="3777c-117">ルール プロバイダーは、設定し、ルール テーブル内のルールを処理します。</span><span class="sxs-lookup"><span data-stu-id="3777c-117">A rule provider sets and handles rules in a rule table.</span></span> <span data-ttu-id="3777c-118">このようなルールが設定されている場合に、遅延されたアクションを処理する手段も用意されています。</span><span class="sxs-lookup"><span data-stu-id="3777c-118">It also provides a means of handling any deferred actions if such rules are set.</span></span> <span data-ttu-id="3777c-119">遅延アクションは、インフォメーション ストアによって暗黙的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="3777c-119">Deferred actions are created implicitly by the information store.</span></span> <span data-ttu-id="3777c-120">別のストアに移動またはコピー操作の場合は、遅延処理のルールを設定するプロバイダーが備わっていること、ルールが実行され、遅延アクションが作成されるときにアクションを実行するハンドラー。</span><span class="sxs-lookup"><span data-stu-id="3777c-120">For move or copy operations to a different store, if a provider sets a deferred action rule, it must provide a handler to perform the action when the rule is fired and a deferred action is created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3777c-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3777c-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3777c-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3777c-122">Protocol specifications</span></span>

<span data-ttu-id="3777c-123">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3777c-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3777c-124">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3777c-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3777c-125">[[MS OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3777c-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3777c-126">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="3777c-126">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3777c-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3777c-127">Header files</span></span>

<span data-ttu-id="3777c-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3777c-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="3777c-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3777c-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="3777c-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3777c-130">Mapitags.h</span></span>
  
> <span data-ttu-id="3777c-131">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3777c-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3777c-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="3777c-132">See also</span></span>



[<span data-ttu-id="3777c-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3777c-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3777c-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3777c-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3777c-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3777c-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3777c-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3777c-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

