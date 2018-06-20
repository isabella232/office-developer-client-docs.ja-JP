---
title: PidTagJunkThreshold の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0f8484e195b1cda8e1d633133cdff89c571d8ecd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802915"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="081ff-103">PidTagJunkThreshold の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="081ff-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="081ff-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="081ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="081ff-105">どの程度積極的に示す [迷惑メール] フォルダーに受信メールを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="081ff-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="081ff-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="081ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="081ff-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="081ff-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="081ff-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="081ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="081ff-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="081ff-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="081ff-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="081ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="081ff-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="081ff-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="081ff-112">領域:</span><span class="sxs-lookup"><span data-stu-id="081ff-112">Area:</span></span>  <br/> |<span data-ttu-id="081ff-113">スパム</span><span class="sxs-lookup"><span data-stu-id="081ff-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="081ff-114">備考</span><span class="sxs-lookup"><span data-stu-id="081ff-114">Remarks</span></span>

<span data-ttu-id="081ff-115">このプロパティは、高と低に対応/の設定にフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="081ff-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="081ff-116">"0 xffffffff"の値は、ブロック リストを適用する必要がありますが、スパム フィルターが適用されないことを示します。</span><span class="sxs-lookup"><span data-stu-id="081ff-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="081ff-117">「0x80000000」値は、すべてのメールはを除き、これらのメッセージの差出人セーフ リストに送信者からの迷惑メールや、信頼された受信者リストの受信者に送信されることを示します。</span><span class="sxs-lookup"><span data-stu-id="081ff-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="081ff-118">この値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="081ff-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="081ff-119">**値**</span><span class="sxs-lookup"><span data-stu-id="081ff-119">**Value**</span></span>|<span data-ttu-id="081ff-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="081ff-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="081ff-121">0 xffffffff</span><span class="sxs-lookup"><span data-stu-id="081ff-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="081ff-122">なしスパムのフィルタ リング</span><span class="sxs-lookup"><span data-stu-id="081ff-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="081ff-123">0x00000006</span><span class="sxs-lookup"><span data-stu-id="081ff-123">0x00000006</span></span>  <br/> |<span data-ttu-id="081ff-124">低い迷惑メールのフィルタ リング</span><span class="sxs-lookup"><span data-stu-id="081ff-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="081ff-125">0x00000003</span><span class="sxs-lookup"><span data-stu-id="081ff-125">0x00000003</span></span>  <br/> |<span data-ttu-id="081ff-126">高い迷惑メールのフィルタ リング</span><span class="sxs-lookup"><span data-stu-id="081ff-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="081ff-127">0x80000000</span><span class="sxs-lookup"><span data-stu-id="081ff-127">0x80000000</span></span>  <br/> |<span data-ttu-id="081ff-128">リストのみ</span><span class="sxs-lookup"><span data-stu-id="081ff-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="081ff-129">関連リソース</span><span class="sxs-lookup"><span data-stu-id="081ff-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="081ff-130">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="081ff-130">Protocol specifications</span></span>

<span data-ttu-id="081ff-131">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="081ff-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="081ff-132">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="081ff-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="081ff-133">[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="081ff-133">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="081ff-134">許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。</span><span class="sxs-lookup"><span data-stu-id="081ff-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="081ff-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="081ff-135">Header files</span></span>

<span data-ttu-id="081ff-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="081ff-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="081ff-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="081ff-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="081ff-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="081ff-138">Mapitags.h</span></span>
  
> <span data-ttu-id="081ff-139">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="081ff-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="081ff-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="081ff-140">See also</span></span>



[<span data-ttu-id="081ff-141">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="081ff-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="081ff-142">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="081ff-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="081ff-143">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="081ff-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="081ff-144">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="081ff-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

