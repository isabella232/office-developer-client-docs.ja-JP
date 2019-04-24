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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 70f09d6db5940fcb9b980cc839988113bd3a3e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316339"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a><span data-ttu-id="cd2f9-103">PidTagExtendedRuleMessageActions 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cd2f9-103">PidTagExtendedRuleMessageActions Canonical Property</span></span>

  
  
<span data-ttu-id="cd2f9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd2f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd2f9-105">フォルダー関連情報 (fai) メッセージで使用される名前付きプロパティについての追加情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cd2f9-105">Contains additional information about the named properties used in a Folder Associated Information (FAI) message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cd2f9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="cd2f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd2f9-107">PR_EXTENDED_RULE_MSG_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="cd2f9-107">PR_EXTENDED_RULE_MSG_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="cd2f9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cd2f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd2f9-109">0x0e99</span><span class="sxs-lookup"><span data-stu-id="cd2f9-109">0x0E99</span></span>  <br/> |
|<span data-ttu-id="cd2f9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="cd2f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd2f9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cd2f9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cd2f9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="cd2f9-112">Area:</span></span>  <br/> |<span data-ttu-id="cd2f9-113">ルール</span><span class="sxs-lookup"><span data-stu-id="cd2f9-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd2f9-114">解説</span><span class="sxs-lookup"><span data-stu-id="cd2f9-114">Remarks</span></span>

<span data-ttu-id="cd2f9-115">このプロパティは、fai メッセージで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd2f9-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="cd2f9-116">このプロパティは、 **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) と同じ目的で使用されますが、ルールのバージョンとルールの処理に格納されている名前付きプロパティについての追加情報に加えて、必要なアクションに関する情報が含まれています。このルールによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="cd2f9-116">This property serves the same purpose as **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), but contains additional information about the version of the rule and the named properties stored in the rule action, as well as information about the actions to be performed by this rule.</span></span> <span data-ttu-id="cd2f9-117">アクションを格納するために使用されるアクションバッファーの一部に含まれるすべての文字列値は、Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd2f9-117">All string values contained in any part of the action buffer used to contain actions must be in Unicode format.</span></span>
  
<span data-ttu-id="cd2f9-118">このバイナリプロパティの形式の詳細については、「 [[OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd2f9-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cd2f9-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cd2f9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cd2f9-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cd2f9-120">Protocol specifications</span></span>

<span data-ttu-id="cd2f9-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd2f9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd2f9-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cd2f9-122">Provides references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="cd2f9-123">[[OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd2f9-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd2f9-124">サーバー上の受信電子メールメッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="cd2f9-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cd2f9-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="cd2f9-125">Header files</span></span>

<span data-ttu-id="cd2f9-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd2f9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd2f9-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cd2f9-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="cd2f9-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="cd2f9-128">Mapitags.h</span></span>
  
> <span data-ttu-id="cd2f9-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cd2f9-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd2f9-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd2f9-130">See also</span></span>



[<span data-ttu-id="cd2f9-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="cd2f9-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd2f9-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cd2f9-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd2f9-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cd2f9-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd2f9-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cd2f9-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

