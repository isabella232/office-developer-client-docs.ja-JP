---
title: PidTagAttachEncoding 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4bda4783012a3a5cd50d9c0aea6a37ccd238b660
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345494"
---
# <a name="pidtagattachencoding-canonical-property"></a><span data-ttu-id="91184-103">PidTagAttachEncoding 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91184-103">PidTagAttachEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="91184-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91184-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91184-105">添付ファイルのエンコーディングを指定する、ASN を含むオブジェクト識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="91184-105">Contains an ASN.1 object identifier that specifies the encoding for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91184-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="91184-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91184-107">PR_ATTACH_ENCODING</span><span class="sxs-lookup"><span data-stu-id="91184-107">PR_ATTACH_ENCODING</span></span>  <br/> |
|<span data-ttu-id="91184-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="91184-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91184-109">0x3702</span><span class="sxs-lookup"><span data-stu-id="91184-109">0x3702</span></span>  <br/> |
|<span data-ttu-id="91184-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="91184-110">Data type:</span></span>  <br/> |<span data-ttu-id="91184-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="91184-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="91184-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="91184-112">Area:</span></span>  <br/> |<span data-ttu-id="91184-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="91184-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91184-114">解説</span><span class="sxs-lookup"><span data-stu-id="91184-114">Remarks</span></span>

<span data-ttu-id="91184-115">このプロパティは、添付ファイル内のデータの変換に使用されるアルゴリズムを識別します。</span><span class="sxs-lookup"><span data-stu-id="91184-115">This property identifies the algorithm used to transform the data in an attachment.</span></span>
  
 <span data-ttu-id="91184-116">**メモ\*\*\*\*PR_ATTACH_ENCODING**プロパティと**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) プロパティを混同しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="91184-116">**Note** The **PR_ATTACH_ENCODING** and **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) properties should not be confused.</span></span> <span data-ttu-id="91184-117">ペアになっていないか、関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="91184-117">They are not paired or related.</span></span> <span data-ttu-id="91184-118">**PR_ATTACH_TAG**は、添付ファイルを最初に生成したアプリケーションを識別します。</span><span class="sxs-lookup"><span data-stu-id="91184-118">**PR_ATTACH_TAG** identifies the application that originally generated the attachment.</span></span> <span data-ttu-id="91184-119">"object" は、用語オブジェクトの識別子、およびオブジェクト指向プログラミングの場合よりも、X でより一般的な意味を持ちます。</span><span class="sxs-lookup"><span data-stu-id="91184-119">"Object" has a much more general meaning in the term object identifier, and in X.400, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="91184-120">オブジェクト識別子の構文とサンプルオブジェクトの識別子は、MAPIOID で定義されています。H ヘッダーファイル。</span><span class="sxs-lookup"><span data-stu-id="91184-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="91184-121">**PR_ATTACH_ENCODING**の値は、MAPIOID で定義されている値に限定されません。H.</span><span class="sxs-lookup"><span data-stu-id="91184-121">Values for **PR_ATTACH_ENCODING** are not limited to those defined in MAPIOID.H.</span></span> <span data-ttu-id="91184-122">たとえば、添付 Macintosh ファイルでは、MacBinary などの識別子を使用できます。</span><span class="sxs-lookup"><span data-stu-id="91184-122">For example, attached Macintosh files can use an identifier such as MacBinary.</span></span> 
  
<span data-ttu-id="91184-123">これらのオブジェクト識別子の詳細については、209個のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="91184-123">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="91184-124">オブジェクト識別子は、ftbp (ファイル転送本文パーツ) 環境のアプリケーション参照要素にあります。</span><span class="sxs-lookup"><span data-stu-id="91184-124">The object identifier is found in the application-reference element of the FTBP (File Transfer Body Part) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="91184-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="91184-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91184-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="91184-126">Protocol specifications</span></span>

<span data-ttu-id="91184-127">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91184-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91184-128">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="91184-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91184-129">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="91184-129">Header files</span></span>

<span data-ttu-id="91184-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91184-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="91184-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="91184-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="91184-132">Mapitags</span><span class="sxs-lookup"><span data-stu-id="91184-132">Mapitags.h</span></span>
  
> <span data-ttu-id="91184-133">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="91184-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91184-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="91184-134">See also</span></span>



[<span data-ttu-id="91184-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="91184-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91184-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91184-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91184-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="91184-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91184-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="91184-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

