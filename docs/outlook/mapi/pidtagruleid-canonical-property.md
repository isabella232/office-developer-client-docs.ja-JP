---
title: PidTagRuleId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 52a6132dcd6aa2c3a2951f3d1a6458808364dccb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803403"
---
# <a name="pidtagruleid-canonical-property"></a><span data-ttu-id="68415-103">PidTagRuleId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="68415-103">PidTagRuleId Canonical Property</span></span>

  
  
<span data-ttu-id="68415-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68415-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68415-105">ルールが最初に作成したとき、各ルールのメッセージング サーバーが生成されます一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="68415-105">Specifies a unique identifier the messaging server generates for each rule when the rule is first created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68415-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="68415-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="68415-107">PR_RULE_ID</span><span class="sxs-lookup"><span data-stu-id="68415-107">PR_RULE_ID</span></span>  <br/> |
|<span data-ttu-id="68415-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="68415-108">Identifier:</span></span>  <br/> |<span data-ttu-id="68415-109">0x6674</span><span class="sxs-lookup"><span data-stu-id="68415-109">0x6674</span></span>  <br/> |
|<span data-ttu-id="68415-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="68415-110">Data type:</span></span>  <br/> |<span data-ttu-id="68415-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="68415-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="68415-112">領域:</span><span class="sxs-lookup"><span data-stu-id="68415-112">Area:</span></span>  <br/> |<span data-ttu-id="68415-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="68415-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68415-114">備考</span><span class="sxs-lookup"><span data-stu-id="68415-114">Remarks</span></span>

<span data-ttu-id="68415-115">新しいを作成するとき、クライアントがこのプロパティを指定する必要がありますルールが変更またはルールを削除するときに指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68415-115">The client must not specify this property when creating a new rule but must specify it when modifying or deleting a rule.</span></span>
  
<span data-ttu-id="68415-116">ルールを削除するとプロパティのみが、クライアントに渡す必要があります**PR_RULE_ID**は、他のすべてのプロパティで渡さないでください。</span><span class="sxs-lookup"><span data-stu-id="68415-116">When deleting a rule, the only property the client must pass is **PR_RULE_ID** and should not pass in any other property.</span></span> <span data-ttu-id="68415-117">サーバーは、このプロパティ以外のプロパティを無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68415-117">The server must ignore properties other than this property.</span></span> <span data-ttu-id="68415-118">ルールを追加するには、クライアントが**PR_RULE_ID**に渡す必要があります。 されません、 **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))、 **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) と**PR_RULE_PROVIDER** ([に渡す必要があります。PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="68415-118">When adding a rule, the client must not pass in **PR_RULE_ID**, it must pass in the **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) and **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) properties.</span></span> <span data-ttu-id="68415-119">ルールを変更するには、クライアントが**PR_RULE_ID**に渡す必要があり、変更する必要があるプロパティの残りの部分に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="68415-119">When modifying a rule, the client must pass in **PR_RULE_ID** and should pass in the rest of the properties that need to be modified.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="68415-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="68415-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="68415-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="68415-121">Protocol specifications</span></span>

<span data-ttu-id="68415-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68415-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68415-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="68415-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="68415-124">[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68415-124">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68415-125">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="68415-125">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="68415-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="68415-126">Header files</span></span>

<span data-ttu-id="68415-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="68415-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="68415-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="68415-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="68415-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="68415-129">Mapitags.h</span></span>
  
> <span data-ttu-id="68415-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="68415-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68415-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="68415-131">See also</span></span>



[<span data-ttu-id="68415-132">PidTagRuleCondition の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="68415-132">PidTagRuleCondition Canonical Property</span></span>](pidtagrulecondition-canonical-property.md)
  
[<span data-ttu-id="68415-133">PidTagRuleActions の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="68415-133">PidTagRuleActions Canonical Property</span></span>](pidtagruleactions-canonical-property.md)
  
[<span data-ttu-id="68415-134">PidTagRuleProvider の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="68415-134">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="68415-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="68415-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68415-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="68415-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68415-137">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="68415-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68415-138">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="68415-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

