---
title: PidTagRuleState 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338613"
---
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="a1ce8-103">PidTagRuleState 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a1ce8-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="a1ce8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1ce8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1ce8-105">ルールの状態を指定するフラグのビットマスクの組み合わせとして解釈される値。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1ce8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a1ce8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1ce8-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="a1ce8-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="a1ce8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a1ce8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a1ce8-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="a1ce8-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="a1ce8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a1ce8-110">Data type:</span></span>  <br/> |<span data-ttu-id="a1ce8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a1ce8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a1ce8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a1ce8-112">Area:</span></span>  <br/> |<span data-ttu-id="a1ce8-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="a1ce8-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1ce8-114">解説</span><span class="sxs-lookup"><span data-stu-id="a1ce8-114">Remarks</span></span>

<span data-ttu-id="a1ce8-115">次の表では、このプロパティに指定できる値を定義します。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="a1ce8-116">EN (ST_ENABLED、ビットマスク 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="a1ce8-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="a1ce8-117">ルールは実行に対して有効になっています。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-117">The rule is enabled for execution.</span></span> <span data-ttu-id="a1ce8-118">このフラグが設定されていない場合、ルールを評価するときに、サーバーはこのルールをスキップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="a1ce8-119">ER (ST_ERROR、ビットマスク 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="a1ce8-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="a1ce8-120">サーバーでルールの処理中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="a1ce8-121">OF (ST_ONLY_WHEN_OOF, ビットマスク 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="a1ce8-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="a1ce8-122">このルールは、ユーザーがメールボックスの不在 (OOF) 状態を設定した場合にのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="a1ce8-123">このフラグは、パブリックフォルダーのルールに設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="a1ce8-124">HI (ST_KEEP_OOF_HIST, ビットマスク 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="a1ce8-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="a1ce8-125">このフラグは、パブリックフォルダーのルールに設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="a1ce8-126">EL (ST_EXIT_LEVEL、ビットマスク 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="a1ce8-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="a1ce8-127">ルールの評価は、不在時ルールの評価を除き、このルールを実行した後に終了します。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="a1ce8-128">SCL (ST_SKIP_IF_SCL_IS_SAFE、ビットマスク 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="a1ce8-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="a1ce8-129">このルールの評価はスキップされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="a1ce8-130">PE (ST_RULE_PARSE_ERROR、ビットマスク 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="a1ce8-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="a1ce8-131">クライアントによって提供されたルールデータの解析中にサーバーでエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="a1ce8-132">X</span><span class="sxs-lookup"><span data-stu-id="a1ce8-132">X</span></span>
  
> <span data-ttu-id="a1ce8-133">このプロトコルでは使用されません。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-133">Unused by this protocol.</span></span> <span data-ttu-id="a1ce8-134">このビットは、クライアントが変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="a1ce8-135">ST_ONLY_WHEN_OOF フラグと ST_EXIT_LEVEL フラグの間の相互作用に関する注意事項:</span><span class="sxs-lookup"><span data-stu-id="a1ce8-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="a1ce8-136">"不在" 状態がメールボックスに設定されており、ルールの条件が TRUE と評価される場合は、</span><span class="sxs-lookup"><span data-stu-id="a1ce8-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="a1ce8-137">そして：</span><span class="sxs-lookup"><span data-stu-id="a1ce8-137">AND:</span></span>
  
- <span data-ttu-id="a1ce8-138">ルールに ST_EXIT_LEVEL フラグが設定されていて、ST_ONLY_WHEN_OOF フラグが設定されていません。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="a1ce8-139">次に、ST_ONLY_WHEN_OOF フラグが設定されていない後続のルールをサーバーが評価しないようにして、ST_ONLY_WHEN_OOF フラグが設定されている後続のルールを評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="a1ce8-140">や</span><span class="sxs-lookup"><span data-stu-id="a1ce8-140">OR:</span></span>
  
- <span data-ttu-id="a1ce8-141">ルールには、ST_EXIT_LEVEL と ST_ONLY_WHEN_OOF の両方のフラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="a1ce8-142">その後、サーバーは後続のルールを評価しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a1ce8-143">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a1ce8-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1ce8-144">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a1ce8-144">Protocol specifications</span></span>

<span data-ttu-id="a1ce8-145">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1ce8-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1ce8-146">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a1ce8-147">[[OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1ce8-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1ce8-148">サーバー上の受信電子メールメッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1ce8-149">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a1ce8-149">Header files</span></span>

<span data-ttu-id="a1ce8-150">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1ce8-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1ce8-151">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="a1ce8-152">Mapitags</span><span class="sxs-lookup"><span data-stu-id="a1ce8-152">Mapitags.h</span></span>
  
> <span data-ttu-id="a1ce8-153">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a1ce8-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1ce8-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1ce8-154">See also</span></span>



[<span data-ttu-id="a1ce8-155">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a1ce8-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1ce8-156">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a1ce8-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1ce8-157">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a1ce8-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1ce8-158">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a1ce8-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

