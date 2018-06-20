---
title: PidTagRuleState の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 519ee2b91275e4253845afa35a9a80470071966d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803428"
---
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="75ea2-103">PidTagRuleState の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="75ea2-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="75ea2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="75ea2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="75ea2-105">ルールの状態を指定するフラグのビットマスクの組み合わせとして解釈される値です。</span><span class="sxs-lookup"><span data-stu-id="75ea2-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75ea2-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="75ea2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75ea2-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="75ea2-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="75ea2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="75ea2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75ea2-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="75ea2-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="75ea2-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="75ea2-110">Data type:</span></span>  <br/> |<span data-ttu-id="75ea2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="75ea2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="75ea2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="75ea2-112">Area:</span></span>  <br/> |<span data-ttu-id="75ea2-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="75ea2-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75ea2-114">備考</span><span class="sxs-lookup"><span data-stu-id="75ea2-114">Remarks</span></span>

<span data-ttu-id="75ea2-115">次の表は、このプロパティの値を定義します。</span><span class="sxs-lookup"><span data-stu-id="75ea2-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="75ea2-116">EN (ST_ENABLED、0x00000001 のビットマスク)</span><span class="sxs-lookup"><span data-stu-id="75ea2-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="75ea2-117">ルールは実行するために有効です。</span><span class="sxs-lookup"><span data-stu-id="75ea2-117">The rule is enabled for execution.</span></span> <span data-ttu-id="75ea2-118">このフラグが設定されていない場合、サーバーでは、ルールを評価するときにこのルールにスキップします。</span><span class="sxs-lookup"><span data-stu-id="75ea2-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="75ea2-119">ER (ST_ERROR、ビットマスク 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="75ea2-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="75ea2-120">サーバーは、ルールを処理中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="75ea2-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="75ea2-121">(ST_ONLY_WHEN_OOF、ビットマスク 0x00000004) の</span><span class="sxs-lookup"><span data-stu-id="75ea2-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="75ea2-122">ルールは、ユーザー メールボックスの不在時の Office (OOF) の状態を設定する場合にのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="75ea2-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="75ea2-123">パブリック フォルダーのルールで、このフラグを設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="75ea2-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="75ea2-124">HI (ST_KEEP_OOF_HIST、ビットマスク 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="75ea2-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="75ea2-125">パブリック フォルダーのルールで、このフラグを設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="75ea2-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="75ea2-126">EL (ST_EXIT_LEVEL、ビットマスク 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="75ea2-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="75ea2-127">ルールの評価は、Office のうち、ルールの評価の場合を除き、この規則を実行した後終了します。</span><span class="sxs-lookup"><span data-stu-id="75ea2-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="75ea2-128">SCL (ST_SKIP_IF_SCL_IS_SAFE、ビットマスク 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="75ea2-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="75ea2-129">このルールの評価をスキップすることがあります。</span><span class="sxs-lookup"><span data-stu-id="75ea2-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="75ea2-130">PE (ST_RULE_PARSE_ERROR、ビットマスク 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="75ea2-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="75ea2-131">サーバー、クライアントによって提供される規則のデータを解析中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="75ea2-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="75ea2-132">X</span><span class="sxs-lookup"><span data-stu-id="75ea2-132">X</span></span>
  
> <span data-ttu-id="75ea2-133">このプロトコルが使用されていません。</span><span class="sxs-lookup"><span data-stu-id="75ea2-133">Unused by this protocol.</span></span> <span data-ttu-id="75ea2-134">クライアントが、このビットを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="75ea2-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="75ea2-135">フラグの ST_ONLY_WHEN_OOF と ST_EXIT_LEVEL 間の相互作用に注意してください。</span><span class="sxs-lookup"><span data-stu-id="75ea2-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="75ea2-136">メールボックスの [不在時の Office"状態に設定し、ルール条件の評価が true の場合、</span><span class="sxs-lookup"><span data-stu-id="75ea2-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="75ea2-137">そして：</span><span class="sxs-lookup"><span data-stu-id="75ea2-137">AND:</span></span>
  
- <span data-ttu-id="75ea2-138">ルールがあり、ST_EXIT_LEVEL フラグを設定、ST_ONLY_WHEN_OOF フラグが設定されていることはありません。</span><span class="sxs-lookup"><span data-stu-id="75ea2-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="75ea2-139">サーバーが ST_ONLY_WHEN_OOF する必要はありません後のルールを評価する必要があります、セットのフラグを設定し、ST_ONLY_WHEN_OOF フラグが設定された後のルールを評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75ea2-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="75ea2-140">OR:</span><span class="sxs-lookup"><span data-stu-id="75ea2-140">OR:</span></span>
  
- <span data-ttu-id="75ea2-141">ルールが、ST_EXIT_LEVEL と ST_ONLY_WHEN_OOF の両方のフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="75ea2-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="75ea2-142">サーバーする必要があります、その後のルールを評価しません。</span><span class="sxs-lookup"><span data-stu-id="75ea2-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="75ea2-143">関連リソース</span><span class="sxs-lookup"><span data-stu-id="75ea2-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75ea2-144">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="75ea2-144">Protocol specifications</span></span>

<span data-ttu-id="75ea2-145">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75ea2-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75ea2-146">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="75ea2-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="75ea2-147">[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75ea2-147">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75ea2-148">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="75ea2-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75ea2-149">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="75ea2-149">Header files</span></span>

<span data-ttu-id="75ea2-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75ea2-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="75ea2-151">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="75ea2-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="75ea2-152">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="75ea2-152">Mapitags.h</span></span>
  
> <span data-ttu-id="75ea2-153">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="75ea2-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75ea2-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="75ea2-154">See also</span></span>



[<span data-ttu-id="75ea2-155">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="75ea2-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75ea2-156">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="75ea2-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75ea2-157">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="75ea2-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75ea2-158">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="75ea2-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

