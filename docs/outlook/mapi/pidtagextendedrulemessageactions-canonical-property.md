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
ms.openlocfilehash: 9b6af0c7fae85a2ea6cbd53159674fdcd32c642c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592770"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a><span data-ttu-id="0bbdd-103">PidTagExtendedRuleMessageActions 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0bbdd-103">PidTagExtendedRuleMessageActions Canonical Property</span></span>

  
  
<span data-ttu-id="0bbdd-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0bbdd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0bbdd-105">フォルダー関連情報 (FAI) メッセージで使用される名前付きプロパティに関する追加情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0bbdd-105">Contains additional information about the named properties used in a Folder Associated Information (FAI) message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0bbdd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0bbdd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0bbdd-107">PR_EXTENDED_RULE_MSG_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="0bbdd-107">PR_EXTENDED_RULE_MSG_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="0bbdd-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0bbdd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0bbdd-109">0x0E99</span><span class="sxs-lookup"><span data-stu-id="0bbdd-109">0x0E99</span></span>  <br/> |
|<span data-ttu-id="0bbdd-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0bbdd-110">Data type:</span></span>  <br/> |<span data-ttu-id="0bbdd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0bbdd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0bbdd-112">領域:</span><span class="sxs-lookup"><span data-stu-id="0bbdd-112">Area:</span></span>  <br/> |<span data-ttu-id="0bbdd-113">Rules</span><span class="sxs-lookup"><span data-stu-id="0bbdd-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bbdd-114">注釈</span><span class="sxs-lookup"><span data-stu-id="0bbdd-114">Remarks</span></span>

<span data-ttu-id="0bbdd-115">このプロパティは、FAI メッセージを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0bbdd-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="0bbdd-116">このプロパティは、 **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) と同じ役目を果たしますが、アクションについての情報と同様に、ルールとルールの処理に保存されている名前付きプロパティのバージョンに関する追加情報が含まれていますこのルールによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="0bbdd-116">This property serves the same purpose as **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), but contains additional information about the version of the rule and the named properties stored in the rule action, as well as information about the actions to be performed by this rule.</span></span> <span data-ttu-id="0bbdd-117">アクションを格納するために使用するアクション バッファーの一部に含まれるすべての文字列値は、Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0bbdd-117">All string values contained in any part of the action buffer used to contain actions must be in Unicode format.</span></span>
  
<span data-ttu-id="0bbdd-118">このバイナリのプロパティの形式については、 [[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0bbdd-118">For information about the format of this binary property, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0bbdd-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0bbdd-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0bbdd-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0bbdd-120">Protocol specifications</span></span>

<span data-ttu-id="0bbdd-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bbdd-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bbdd-122">関連する Exchange Server プロトコルの仕様への参照が用意されています。</span><span class="sxs-lookup"><span data-stu-id="0bbdd-122">Provides references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="0bbdd-123">[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bbdd-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bbdd-124">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="0bbdd-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0bbdd-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0bbdd-125">Header files</span></span>

<span data-ttu-id="0bbdd-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0bbdd-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0bbdd-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0bbdd-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="0bbdd-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0bbdd-128">Mapitags.h</span></span>
  
> <span data-ttu-id="0bbdd-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0bbdd-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0bbdd-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="0bbdd-130">See also</span></span>



[<span data-ttu-id="0bbdd-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0bbdd-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0bbdd-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0bbdd-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0bbdd-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0bbdd-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0bbdd-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0bbdd-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

