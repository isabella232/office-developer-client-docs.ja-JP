---
title: PidTagRuleId 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8d88838893836c550136be9556299258b44e3e49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359494"
---
# <a name="pidtagruleid-canonical-property"></a><span data-ttu-id="6836e-103">PidTagRuleId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6836e-103">PidTagRuleId Canonical Property</span></span>

  
  
<span data-ttu-id="6836e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6836e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6836e-105">ルールの最初の作成時にメッセージング サーバーが各ルールに対して生成する一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="6836e-105">Specifies a unique identifier the messaging server generates for each rule when the rule is first created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6836e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6836e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6836e-107">PR_RULE_ID</span><span class="sxs-lookup"><span data-stu-id="6836e-107">PR_RULE_ID</span></span>  <br/> |
|<span data-ttu-id="6836e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6836e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6836e-109">0x6674</span><span class="sxs-lookup"><span data-stu-id="6836e-109">0x6674</span></span>  <br/> |
|<span data-ttu-id="6836e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6836e-110">Data type:</span></span>  <br/> |<span data-ttu-id="6836e-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="6836e-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="6836e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="6836e-112">Area:</span></span>  <br/> |<span data-ttu-id="6836e-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="6836e-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6836e-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6836e-114">Remarks</span></span>

<span data-ttu-id="6836e-115">クライアントは、新しいルールを作成するときにこのプロパティを指定する必要がありますが、ルールを変更または削除するときに指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6836e-115">The client must not specify this property when creating a new rule but must specify it when modifying or deleting a rule.</span></span>
  
<span data-ttu-id="6836e-116">ルールを削除する場合、クライアントが渡す必要がある唯一のプロパティはPR_RULE_IDプロパティを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6836e-116">When deleting a rule, the only property the client must pass is **PR_RULE_ID** and should not pass in any other property.</span></span> <span data-ttu-id="6836e-117">サーバーは、このプロパティ以外のプロパティを無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6836e-117">The server must ignore properties other than this property.</span></span> <span data-ttu-id="6836e-118">ルールを追加する場合、クライアントは **PR_RULE_ID** で渡す必要があります。PR_RULE_CONDITION (  [PidTagRuleCondition](pidtagrulecondition-canonical-property.md)) **、PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) プロパティ、および PR_RULE_PROVIDER **(** [PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) プロパティを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6836e-118">When adding a rule, the client must not pass in **PR_RULE_ID**, it must pass in the **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) and **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) properties.</span></span> <span data-ttu-id="6836e-119">ルールを変更する場合、クライアントは PR_RULE_IDを渡す必要があります。変更する必要がある他のプロパティを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6836e-119">When modifying a rule, the client must pass in **PR_RULE_ID** and should pass in the rest of the properties that need to be modified.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6836e-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6836e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6836e-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6836e-121">Protocol specifications</span></span>

<span data-ttu-id="6836e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6836e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6836e-123">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="6836e-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6836e-124">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6836e-124">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6836e-125">サーバー上の受信メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="6836e-125">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6836e-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6836e-126">Header files</span></span>

<span data-ttu-id="6836e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6836e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6836e-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6836e-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="6836e-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6836e-129">Mapitags.h</span></span>
  
> <span data-ttu-id="6836e-130">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="6836e-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6836e-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="6836e-131">See also</span></span>



[<span data-ttu-id="6836e-132">PidTagRuleCondition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6836e-132">PidTagRuleCondition Canonical Property</span></span>](pidtagrulecondition-canonical-property.md)
  
[<span data-ttu-id="6836e-133">PidTagRuleActions 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6836e-133">PidTagRuleActions Canonical Property</span></span>](pidtagruleactions-canonical-property.md)
  
[<span data-ttu-id="6836e-134">PidTagRuleProvider 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6836e-134">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="6836e-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6836e-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6836e-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6836e-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6836e-137">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="6836e-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6836e-138">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="6836e-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

