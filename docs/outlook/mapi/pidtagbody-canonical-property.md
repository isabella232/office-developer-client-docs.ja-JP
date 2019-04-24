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
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326636"
---
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="c3a90-103">PidTagBody 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c3a90-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="c3a90-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3a90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3a90-105">メッセージテキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c3a90-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c3a90-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c3a90-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c3a90-107">PR_BODY、PR_BODY_A、PR_BODY_W</span><span class="sxs-lookup"><span data-stu-id="c3a90-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="c3a90-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c3a90-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c3a90-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="c3a90-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="c3a90-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c3a90-110">Data type:</span></span>  <br/> |<span data-ttu-id="c3a90-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c3a90-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="c3a90-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c3a90-112">Area:</span></span>  <br/> |<span data-ttu-id="c3a90-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="c3a90-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3a90-114">解説</span><span class="sxs-lookup"><span data-stu-id="c3a90-114">Remarks</span></span>

<span data-ttu-id="c3a90-115">これらのプロパティは、通常、個人間メッセージ (IPM) でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="c3a90-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="c3a90-116">リッチテキスト形式 (RTF) をサポートするメッセージストアは、メッセージテキスト内の空白への変更を無視します。</span><span class="sxs-lookup"><span data-stu-id="c3a90-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="c3a90-117">**PR_BODY**が初めて保存されると、メッセージストアは、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティ (RTF バージョンのメッセージテキスト) も生成して保存します。</span><span class="sxs-lookup"><span data-stu-id="c3a90-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="c3a90-118">[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドが呼び出され、 **PR_BODY**が変更されている場合、メッセージストアは[rtfsync](rtfsync.md)関数を呼び出して RTF バージョンとの同期を確実に行います。</span><span class="sxs-lookup"><span data-stu-id="c3a90-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="c3a90-119">空白のみが変更された場合、プロパティは変更されません。</span><span class="sxs-lookup"><span data-stu-id="c3a90-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="c3a90-120">これにより、メッセージが rtf に対応していないクライアントおよびメッセージングシステムを経由するときに、重要な RTF 形式がすべて保持されます。</span><span class="sxs-lookup"><span data-stu-id="c3a90-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="c3a90-121">このプロパティの値は、MAPI が実行されているオペレーティングシステムのコードページで記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3a90-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c3a90-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c3a90-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c3a90-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c3a90-123">Protocol specifications</span></span>

<span data-ttu-id="c3a90-124">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3a90-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3a90-125">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3a90-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c3a90-126">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3a90-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3a90-127">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="c3a90-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c3a90-128">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c3a90-128">Header files</span></span>

<span data-ttu-id="c3a90-129">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c3a90-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="c3a90-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3a90-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="c3a90-131">Mapitags</span><span class="sxs-lookup"><span data-stu-id="c3a90-131">Mapitags.h</span></span>
  
> <span data-ttu-id="c3a90-132">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c3a90-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3a90-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="c3a90-133">See also</span></span>



[<span data-ttu-id="c3a90-134">PidTagRtfInSync 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c3a90-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="c3a90-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c3a90-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c3a90-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c3a90-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c3a90-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c3a90-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c3a90-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c3a90-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

