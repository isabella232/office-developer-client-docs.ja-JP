---
title: PidTagJunkThreshold 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 078dfcc7c24870cf95a2a4b2385c34fbeb64fac0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326853"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="5cf8b-103">PidTagJunkThreshold 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5cf8b-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="5cf8b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5cf8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5cf8b-105">迷惑メール フォルダーに受信メールを積極的に送信する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5cf8b-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5cf8b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5cf8b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5cf8b-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="5cf8b-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="5cf8b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5cf8b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5cf8b-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="5cf8b-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="5cf8b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5cf8b-110">Data type:</span></span>  <br/> |<span data-ttu-id="5cf8b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5cf8b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5cf8b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5cf8b-112">Area:</span></span>  <br/> |<span data-ttu-id="5cf8b-113">スパム</span><span class="sxs-lookup"><span data-stu-id="5cf8b-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5cf8b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5cf8b-114">Remarks</span></span>

<span data-ttu-id="5cf8b-115">このプロパティは、高/低/なしフィルターの設定に対応します。</span><span class="sxs-lookup"><span data-stu-id="5cf8b-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="5cf8b-116">"0xFFFFFFFF" の値は、スパム フィルターを適用しない必要があるが、ブロック リストを適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cf8b-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="5cf8b-117">"0x80000000" の値は、信頼できる送信者リストの送信者からのメッセージ、または信頼できる受信者リストの受信者に送信されたメッセージを除く、すべてのメールがスパムである場合を示します。</span><span class="sxs-lookup"><span data-stu-id="5cf8b-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="5cf8b-118">この値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5cf8b-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="5cf8b-119">**値**</span><span class="sxs-lookup"><span data-stu-id="5cf8b-119">**Value**</span></span>|<span data-ttu-id="5cf8b-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="5cf8b-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5cf8b-121">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="5cf8b-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="5cf8b-122">スパム フィルターなし</span><span class="sxs-lookup"><span data-stu-id="5cf8b-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="5cf8b-123">0x00000006</span><span class="sxs-lookup"><span data-stu-id="5cf8b-123">0x00000006</span></span>  <br/> |<span data-ttu-id="5cf8b-124">低スパム フィルター</span><span class="sxs-lookup"><span data-stu-id="5cf8b-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="5cf8b-125">0x00000003</span><span class="sxs-lookup"><span data-stu-id="5cf8b-125">0x00000003</span></span>  <br/> |<span data-ttu-id="5cf8b-126">高いスパム フィルター</span><span class="sxs-lookup"><span data-stu-id="5cf8b-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="5cf8b-127">0x80000000</span><span class="sxs-lookup"><span data-stu-id="5cf8b-127">0x80000000</span></span>  <br/> |<span data-ttu-id="5cf8b-128">信頼できるリストのみ</span><span class="sxs-lookup"><span data-stu-id="5cf8b-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5cf8b-129">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5cf8b-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5cf8b-130">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5cf8b-130">Protocol specifications</span></span>

<span data-ttu-id="5cf8b-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cf8b-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cf8b-132">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="5cf8b-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5cf8b-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cf8b-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cf8b-134">許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="5cf8b-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5cf8b-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5cf8b-135">Header files</span></span>

<span data-ttu-id="5cf8b-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5cf8b-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="5cf8b-137">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5cf8b-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="5cf8b-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5cf8b-138">Mapitags.h</span></span>
  
> <span data-ttu-id="5cf8b-139">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="5cf8b-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5cf8b-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="5cf8b-140">See also</span></span>



[<span data-ttu-id="5cf8b-141">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5cf8b-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5cf8b-142">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5cf8b-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5cf8b-143">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5cf8b-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5cf8b-144">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5cf8b-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

