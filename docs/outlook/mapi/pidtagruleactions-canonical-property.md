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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278901"
---
# <a name="pidtagruleactions-canonical-property"></a><span data-ttu-id="706e0-103">PidTagRuleActions 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="706e0-103">PidTagRuleActions Canonical Property</span></span>

  
  
<span data-ttu-id="706e0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="706e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="706e0-105">ルールに関連付けられているアクションのセットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="706e0-105">Contains the set of actions associated with the rule.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="706e0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="706e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="706e0-107">PR_RULE_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="706e0-107">PR_RULE_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="706e0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="706e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="706e0-109">0x6680</span><span class="sxs-lookup"><span data-stu-id="706e0-109">0x6680</span></span>  <br/> |
|<span data-ttu-id="706e0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="706e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="706e0-111">PT_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="706e0-111">PT_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="706e0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="706e0-112">Area:</span></span>  <br/> |<span data-ttu-id="706e0-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="706e0-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="706e0-114">解説</span><span class="sxs-lookup"><span data-stu-id="706e0-114">Remarks</span></span>

<span data-ttu-id="706e0-115">アクションはルールの処理として表現され、プロパティ値バッファーには、 [[OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)で指定されたとおりにパッケージ化されたルールアクションデータバッファー構造が含まれます。</span><span class="sxs-lookup"><span data-stu-id="706e0-115">The actions are expressed as a rule action and the property value buffer contains the rule action data buffer structure packaged as specified in [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="706e0-116">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="706e0-116">MFCMAPI reference</span></span>

<span data-ttu-id="706e0-117">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="706e0-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="706e0-118">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="706e0-118">**File**</span></span>|<span data-ttu-id="706e0-119">**関数**</span><span class="sxs-lookup"><span data-stu-id="706e0-119">**Function**</span></span>|<span data-ttu-id="706e0-120">**コメント**</span><span class="sxs-lookup"><span data-stu-id="706e0-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="706e0-121">importprocs</span><span class="sxs-lookup"><span data-stu-id="706e0-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="706e0-122">propcopymore、hrcopyactions</span><span class="sxs-lookup"><span data-stu-id="706e0-122">PropCopyMore, HrCopyActions</span></span>  <br/> |<span data-ttu-id="706e0-123">これらの関数は、別のプロパティにコピーする目的で PT_ACTIONS プロパティを解析する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="706e0-123">These functions demonstrate how to parse a PT_ACTIONS property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="706e0-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="706e0-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="706e0-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="706e0-125">Protocol specifications</span></span>

<span data-ttu-id="706e0-126">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="706e0-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="706e0-127">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="706e0-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="706e0-128">[[OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="706e0-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="706e0-129">サーバー上の受信電子メールメッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="706e0-129">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="706e0-130">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="706e0-130">Header files</span></span>

<span data-ttu-id="706e0-131">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="706e0-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="706e0-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="706e0-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="706e0-133">Mapitags</span><span class="sxs-lookup"><span data-stu-id="706e0-133">Mapitags.h</span></span>
  
> <span data-ttu-id="706e0-134">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="706e0-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="706e0-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="706e0-135">See also</span></span>



[<span data-ttu-id="706e0-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="706e0-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="706e0-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="706e0-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="706e0-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="706e0-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="706e0-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="706e0-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

