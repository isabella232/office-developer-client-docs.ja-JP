---
title: PidTagRuleActions 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleActions
api_type:
- COM
ms.assetid: 3ec4259a-8fe9-46c3-82b8-42c6907b8515
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ab246414f7caaf76f462d9b80e762fe614c77c21
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390010"
---
# <a name="pidtagruleactions-canonical-property"></a><span data-ttu-id="2415e-103">PidTagRuleActions 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2415e-103">PidTagRuleActions Canonical Property</span></span>

  
  
<span data-ttu-id="2415e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2415e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2415e-105">ルールに関連付けられたアクションのセットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2415e-105">Contains the set of actions associated with the rule.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2415e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2415e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2415e-107">PR_RULE_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="2415e-107">PR_RULE_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="2415e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2415e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2415e-109">0x6680</span><span class="sxs-lookup"><span data-stu-id="2415e-109">0x6680</span></span>  <br/> |
|<span data-ttu-id="2415e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2415e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2415e-111">PT_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="2415e-111">PT_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="2415e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2415e-112">Area:</span></span>  <br/> |<span data-ttu-id="2415e-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="2415e-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2415e-114">備考</span><span class="sxs-lookup"><span data-stu-id="2415e-114">Remarks</span></span>

<span data-ttu-id="2415e-115">アクションは、ルールの動作として表現し、プロパティ値のバッファーには、 [[MS OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)で指定されているパッケージ化されたルールのアクションのデータ バッファー構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2415e-115">The actions are expressed as a rule action and the property value buffer contains the rule action data buffer structure packaged as specified in [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2415e-116">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="2415e-116">MFCMAPI reference</span></span>

<span data-ttu-id="2415e-117">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2415e-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2415e-118">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="2415e-118">**File**</span></span>|<span data-ttu-id="2415e-119">**関数**</span><span class="sxs-lookup"><span data-stu-id="2415e-119">**Function**</span></span>|<span data-ttu-id="2415e-120">**コメント**</span><span class="sxs-lookup"><span data-stu-id="2415e-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2415e-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="2415e-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="2415e-122">PropCopyMore、HrCopyActions</span><span class="sxs-lookup"><span data-stu-id="2415e-122">PropCopyMore, HrCopyActions</span></span>  <br/> |<span data-ttu-id="2415e-123">これらの関数は、別のプロパティにコピーするために PT_ACTIONS プロパティを解析する方法をデモンストレーションします。</span><span class="sxs-lookup"><span data-stu-id="2415e-123">These functions demonstrate how to parse a PT_ACTIONS property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2415e-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2415e-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2415e-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2415e-125">Protocol specifications</span></span>

<span data-ttu-id="2415e-126">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2415e-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2415e-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2415e-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2415e-128">[[MS OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2415e-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2415e-129">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="2415e-129">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2415e-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2415e-130">Header files</span></span>

<span data-ttu-id="2415e-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2415e-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="2415e-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2415e-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="2415e-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2415e-133">Mapitags.h</span></span>
  
> <span data-ttu-id="2415e-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2415e-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2415e-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="2415e-135">See also</span></span>



[<span data-ttu-id="2415e-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2415e-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2415e-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2415e-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2415e-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2415e-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2415e-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2415e-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

