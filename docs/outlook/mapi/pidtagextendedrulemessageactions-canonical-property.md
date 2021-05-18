---
title: PidTagExtendedRuleMessageActions 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageActions
api_type:
- HeaderDef
ms.assetid: 1cf277d4-76ec-4902-9e54-f1780cee49bf
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 70f09d6db5940fcb9b980cc839988113bd3a3e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316339"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a><span data-ttu-id="af0f5-103">PidTagExtendedRuleMessageActions 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="af0f5-103">PidTagExtendedRuleMessageActions Canonical Property</span></span>

  
  
<span data-ttu-id="af0f5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af0f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af0f5-105">フォルダー関連情報 (FAI) メッセージで使用される名前付きプロパティに関する追加情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="af0f5-105">Contains additional information about the named properties used in a Folder Associated Information (FAI) message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af0f5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="af0f5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af0f5-107">PR_EXTENDED_RULE_MSG_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="af0f5-107">PR_EXTENDED_RULE_MSG_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="af0f5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="af0f5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af0f5-109">0x0E99</span><span class="sxs-lookup"><span data-stu-id="af0f5-109">0x0E99</span></span>  <br/> |
|<span data-ttu-id="af0f5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="af0f5-110">Data type:</span></span>  <br/> |<span data-ttu-id="af0f5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="af0f5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="af0f5-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="af0f5-112">Area:</span></span>  <br/> |<span data-ttu-id="af0f5-113">ルール</span><span class="sxs-lookup"><span data-stu-id="af0f5-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af0f5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="af0f5-114">Remarks</span></span>

<span data-ttu-id="af0f5-115">このプロパティは、FAI メッセージで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af0f5-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="af0f5-116">このプロパティは **、PR_RULE_ACTIONS** ([PidTagRuleActions)](pidtagruleactions-canonical-property.md)と同じ目的を持っていますが、ルールアクションに格納されているルールのバージョンと名前付きプロパティに関する追加情報と、このルールによって実行されるアクションに関する情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="af0f5-116">This property serves the same purpose as **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), but contains additional information about the version of the rule and the named properties stored in the rule action, as well as information about the actions to be performed by this rule.</span></span> <span data-ttu-id="af0f5-117">アクションを含むアクション バッファーの任意の部分に含まれるすべての文字列値は、Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="af0f5-117">All string values contained in any part of the action buffer used to contain actions must be in Unicode format.</span></span>
  
<span data-ttu-id="af0f5-118">このバイナリ プロパティの形式については [、「[MS-OXORULE] 」を参照してください](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="af0f5-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="af0f5-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="af0f5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af0f5-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="af0f5-120">Protocol specifications</span></span>

<span data-ttu-id="af0f5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af0f5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af0f5-122">関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="af0f5-122">Provides references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="af0f5-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af0f5-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af0f5-124">サーバー上の受信メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="af0f5-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af0f5-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="af0f5-125">Header files</span></span>

<span data-ttu-id="af0f5-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af0f5-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="af0f5-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="af0f5-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="af0f5-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="af0f5-128">Mapitags.h</span></span>
  
> <span data-ttu-id="af0f5-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="af0f5-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af0f5-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="af0f5-130">See also</span></span>



[<span data-ttu-id="af0f5-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="af0f5-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af0f5-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="af0f5-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af0f5-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="af0f5-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af0f5-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="af0f5-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

