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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 078dfcc7c24870cf95a2a4b2385c34fbeb64fac0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326853"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="c7613-103">PidTagJunkThreshold 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7613-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="c7613-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7613-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7613-105">迷惑メールフォルダーに受信メールをどれだけ積極的に送信するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c7613-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7613-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c7613-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c7613-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="c7613-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="c7613-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c7613-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c7613-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="c7613-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="c7613-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c7613-110">Data type:</span></span>  <br/> |<span data-ttu-id="c7613-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c7613-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c7613-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c7613-112">Area:</span></span>  <br/> |<span data-ttu-id="c7613-113">スパム</span><span class="sxs-lookup"><span data-stu-id="c7613-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7613-114">解説</span><span class="sxs-lookup"><span data-stu-id="c7613-114">Remarks</span></span>

<span data-ttu-id="c7613-115">このプロパティは、高/低/なしフィルターの設定に対応しています。</span><span class="sxs-lookup"><span data-stu-id="c7613-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="c7613-116">値 "0xffffffff" は、スパムフィルターを適用しない場合でも、ブロックリストを適用する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="c7613-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="c7613-117">値 "0x80000000" は、[信頼できる差出人のリストの送信者からのメッセージを除くすべてのメールがスパムである] または [信頼できる受信者] リストの受信者に送信されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="c7613-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="c7613-118">この値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c7613-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="c7613-119">**値**</span><span class="sxs-lookup"><span data-stu-id="c7613-119">**Value**</span></span>|<span data-ttu-id="c7613-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="c7613-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7613-121">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="c7613-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="c7613-122">スパムフィルターを適用しない</span><span class="sxs-lookup"><span data-stu-id="c7613-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="c7613-123">0x00000006</span><span class="sxs-lookup"><span data-stu-id="c7613-123">0x00000006</span></span>  <br/> |<span data-ttu-id="c7613-124">低スパムフィルター</span><span class="sxs-lookup"><span data-stu-id="c7613-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="c7613-125">0x00000003</span><span class="sxs-lookup"><span data-stu-id="c7613-125">0x00000003</span></span>  <br/> |<span data-ttu-id="c7613-126">高スパムフィルター</span><span class="sxs-lookup"><span data-stu-id="c7613-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="c7613-127">0x80000000</span><span class="sxs-lookup"><span data-stu-id="c7613-127">0x80000000</span></span>  <br/> |<span data-ttu-id="c7613-128">信頼できる一覧のみ</span><span class="sxs-lookup"><span data-stu-id="c7613-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c7613-129">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c7613-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7613-130">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c7613-130">Protocol specifications</span></span>

<span data-ttu-id="c7613-131">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7613-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7613-132">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c7613-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c7613-133">[[OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7613-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7613-134">許可/ブロックリストの処理と、迷惑メールメッセージの決定を有効にします。</span><span class="sxs-lookup"><span data-stu-id="c7613-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7613-135">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c7613-135">Header files</span></span>

<span data-ttu-id="c7613-136">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7613-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7613-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c7613-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="c7613-138">Mapitags</span><span class="sxs-lookup"><span data-stu-id="c7613-138">Mapitags.h</span></span>
  
> <span data-ttu-id="c7613-139">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7613-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7613-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7613-140">See also</span></span>



[<span data-ttu-id="c7613-141">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c7613-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7613-142">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7613-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7613-143">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c7613-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7613-144">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c7613-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

