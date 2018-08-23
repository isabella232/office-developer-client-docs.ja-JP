---
title: PidTagBody 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cbcfdf44044e3cf9e42b0f0503928c9f8720ec1f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574420"
---
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="b1621-103">PidTagBody 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1621-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="b1621-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1621-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1621-105">メッセージ テキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b1621-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1621-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b1621-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1621-107">PR_BODY、PR_BODY_A、PR_BODY_W</span><span class="sxs-lookup"><span data-stu-id="b1621-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="b1621-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b1621-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b1621-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="b1621-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="b1621-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b1621-110">Data type:</span></span>  <br/> |<span data-ttu-id="b1621-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="b1621-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="b1621-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b1621-112">Area:</span></span>  <br/> |<span data-ttu-id="b1621-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="b1621-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1621-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b1621-114">Remarks</span></span>

<span data-ttu-id="b1621-115">これらのプロパティは通常、個人間メッセージ (IPM) でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="b1621-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="b1621-116">リッチ テキスト形式 (RTF) をサポートしているメッセージ ・ ストアは、メッセージのテキスト内の空白への変更を無視します。</span><span class="sxs-lookup"><span data-stu-id="b1621-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="b1621-117">**PR_BODY**が最初に保存されると、メッセージ ・ ストアも生成し、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティ、RTF 形式のメッセージ テキストを格納します。</span><span class="sxs-lookup"><span data-stu-id="b1621-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="b1621-118">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出された後で、 **PR_BODY**が変更された場合は、メッセージ ・ ストアは、rtf 形式のバージョンとの同期を確実に[行う](rtfsync.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b1621-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="b1621-119">プロパティを左の空白が変更されているだけの場合そのままです。</span><span class="sxs-lookup"><span data-stu-id="b1621-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="b1621-120">これには、任意の複雑な RTF メッセージが RTF に対応していないクライアントを通過するときの書式を設定して、メッセージング システムが保持されます。</span><span class="sxs-lookup"><span data-stu-id="b1621-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="b1621-121">MAPI がで実行されているオペレーティング システムのコード ページでは、このプロパティの値を表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1621-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b1621-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b1621-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1621-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b1621-123">Protocol specifications</span></span>

<span data-ttu-id="b1621-124">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1621-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1621-125">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1621-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1621-126">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1621-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1621-127">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="b1621-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1621-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b1621-128">Header files</span></span>

<span data-ttu-id="b1621-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1621-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1621-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1621-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="b1621-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b1621-131">Mapitags.h</span></span>
  
> <span data-ttu-id="b1621-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b1621-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1621-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1621-133">See also</span></span>



[<span data-ttu-id="b1621-134">PidTagRtfInSync 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1621-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="b1621-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1621-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1621-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1621-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1621-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b1621-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1621-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b1621-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

