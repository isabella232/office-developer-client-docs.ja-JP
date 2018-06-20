---
title: PidTagRuleProvider の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5456e0abffd1ac25983809d32fde88644eaa01cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803422"
---
# <a name="pidtagruleprovider-canonical-property"></a><span data-ttu-id="2cd24-103">PidTagRuleProvider の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="2cd24-103">PidTagRuleProvider Canonical Property</span></span>

  
  
<span data-ttu-id="2cd24-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2cd24-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2cd24-105">ルールを設定するアプリケーションの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2cd24-105">Contains the name of the application that sets a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2cd24-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="2cd24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2cd24-107">PR_RULE_PROVIDER、PR_RULE_PROVIDER_A、PR_RULE_PROVIDER_W</span><span class="sxs-lookup"><span data-stu-id="2cd24-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span></span>  <br/> |
|<span data-ttu-id="2cd24-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2cd24-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2cd24-109">0x6681</span><span class="sxs-lookup"><span data-stu-id="2cd24-109">0x6681</span></span>  <br/> |
|<span data-ttu-id="2cd24-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="2cd24-110">Data type:</span></span>  <br/> |<span data-ttu-id="2cd24-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2cd24-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2cd24-112">領域:</span><span class="sxs-lookup"><span data-stu-id="2cd24-112">Area:</span></span>  <br/> |<span data-ttu-id="2cd24-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="2cd24-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2cd24-114">備考</span><span class="sxs-lookup"><span data-stu-id="2cd24-114">Remarks</span></span>

<span data-ttu-id="2cd24-115">これらのコードを識別するプロパティを解釈し、規則の操作を実行する必要がありますアクションの必要性を延期します。</span><span class="sxs-lookup"><span data-stu-id="2cd24-115">Deferred actions need these properties to identify the code that must interpret and execute the rule action.</span></span>
  
<span data-ttu-id="2cd24-116">メールボックスおよびフォルダーに格納されているルールは、ルールのプロバイダー文字列でそれらを所有するアプリケーションに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="2cd24-116">Rules stored on mailboxes and folders are associated with the application that owns them by a rule provider string.</span></span> <span data-ttu-id="2cd24-117">ルール プロバイダーは、設定し、ルール テーブル内のルールを処理します。</span><span class="sxs-lookup"><span data-stu-id="2cd24-117">A rule provider sets and handles rules in a rule table.</span></span> <span data-ttu-id="2cd24-118">このようなルールが設定されている場合に、遅延されたアクションを処理する手段も用意されています。</span><span class="sxs-lookup"><span data-stu-id="2cd24-118">It also provides a means of handling any deferred actions if such rules are set.</span></span> <span data-ttu-id="2cd24-119">遅延アクションは、インフォメーション ストアによって暗黙的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="2cd24-119">Deferred actions are created implicitly by the information store.</span></span> <span data-ttu-id="2cd24-120">別のストアに移動またはコピー操作の場合は、遅延処理のルールを設定するプロバイダーが備わっていること、ルールが実行され、遅延アクションが作成されるときにアクションを実行するハンドラー。</span><span class="sxs-lookup"><span data-stu-id="2cd24-120">For move or copy operations to a different store, if a provider sets a deferred action rule, it must provide a handler to perform the action when the rule is fired and a deferred action is created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2cd24-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2cd24-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2cd24-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2cd24-122">Protocol specifications</span></span>

<span data-ttu-id="2cd24-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2cd24-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2cd24-124">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2cd24-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2cd24-125">[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2cd24-125">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2cd24-126">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="2cd24-126">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2cd24-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2cd24-127">Header files</span></span>

<span data-ttu-id="2cd24-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2cd24-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="2cd24-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2cd24-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="2cd24-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2cd24-130">Mapitags.h</span></span>
  
> <span data-ttu-id="2cd24-131">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2cd24-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2cd24-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="2cd24-132">See also</span></span>



[<span data-ttu-id="2cd24-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2cd24-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2cd24-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2cd24-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2cd24-135">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="2cd24-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2cd24-136">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="2cd24-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

