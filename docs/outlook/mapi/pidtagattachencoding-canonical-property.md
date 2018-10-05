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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382772"
---
# <a name="pidtagattachencoding-canonical-property"></a><span data-ttu-id="4c35c-103">PidTagAttachEncoding 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4c35c-103">PidTagAttachEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="4c35c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c35c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c35c-105">添付ファイルのエンコーディングを指定する ASN.1 オブジェクト識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4c35c-105">Contains an ASN.1 object identifier that specifies the encoding for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c35c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4c35c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c35c-107">PR_ATTACH_ENCODING</span><span class="sxs-lookup"><span data-stu-id="4c35c-107">PR_ATTACH_ENCODING</span></span>  <br/> |
|<span data-ttu-id="4c35c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4c35c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c35c-109">0x3702</span><span class="sxs-lookup"><span data-stu-id="4c35c-109">0x3702</span></span>  <br/> |
|<span data-ttu-id="4c35c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4c35c-110">Data type:</span></span>  <br/> |<span data-ttu-id="4c35c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4c35c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4c35c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4c35c-112">Area:</span></span>  <br/> |<span data-ttu-id="4c35c-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="4c35c-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c35c-114">備考</span><span class="sxs-lookup"><span data-stu-id="4c35c-114">Remarks</span></span>

<span data-ttu-id="4c35c-115">このプロパティは、添付ファイル内のデータを変換するためのアルゴリズムを識別します。</span><span class="sxs-lookup"><span data-stu-id="4c35c-115">This property identifies the algorithm used to transform the data in an attachment.</span></span>
  
 <span data-ttu-id="4c35c-116">**メモ\*\*\*\*PR_ATTACH_ENCODING**および**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) のプロパティとは違います。</span><span class="sxs-lookup"><span data-stu-id="4c35c-116">**Note** The **PR_ATTACH_ENCODING** and **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) properties should not be confused.</span></span> <span data-ttu-id="4c35c-117">ペアにしたり、関連にはしないでください。</span><span class="sxs-lookup"><span data-stu-id="4c35c-117">They are not paired or related.</span></span> <span data-ttu-id="4c35c-118">**PR_ATTACH_TAG**は、最初の添付ファイルを生成したアプリケーションを識別します。</span><span class="sxs-lookup"><span data-stu-id="4c35c-118">**PR_ATTACH_TAG** identifies the application that originally generated the attachment.</span></span> <span data-ttu-id="4c35c-119">「オブジェクト」には、オブジェクト指向プログラミングでよりもより一般的な意味では、用語のオブジェクト識別子では X.400 があります。</span><span class="sxs-lookup"><span data-stu-id="4c35c-119">"Object" has a much more general meaning in the term object identifier, and in X.400, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="4c35c-120">オブジェクトの識別子の構文と例のオブジェクト識別子は、MAPIOID で定義されます。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="4c35c-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="4c35c-121">**PR_ATTACH_ENCODING**の値は、MAPIOID で定義されている制限付きではありません。H.</span><span class="sxs-lookup"><span data-stu-id="4c35c-121">Values for **PR_ATTACH_ENCODING** are not limited to those defined in MAPIOID.H.</span></span> <span data-ttu-id="4c35c-122">たとえば、Macintosh の添付ファイルは、MacBinary など識別子を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="4c35c-122">For example, attached Macintosh files can use an identifier such as MacBinary.</span></span> 
  
<span data-ttu-id="4c35c-123">これらのオブジェクト識別子の詳細については、ASN.1、X.208、X.209 のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c35c-123">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="4c35c-124">FTBP (ファイル転送のボディ部) 環境の要素の参照がアプリケーションのオブジェクト識別子が検索されます。</span><span class="sxs-lookup"><span data-stu-id="4c35c-124">The object identifier is found in the application-reference element of the FTBP (File Transfer Body Part) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4c35c-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4c35c-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4c35c-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4c35c-126">Protocol specifications</span></span>

<span data-ttu-id="4c35c-127">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c35c-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c35c-128">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="4c35c-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4c35c-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4c35c-129">Header files</span></span>

<span data-ttu-id="4c35c-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c35c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c35c-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4c35c-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c35c-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4c35c-132">Mapitags.h</span></span>
  
> <span data-ttu-id="4c35c-133">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4c35c-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c35c-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="4c35c-134">See also</span></span>



[<span data-ttu-id="4c35c-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4c35c-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c35c-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4c35c-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c35c-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4c35c-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c35c-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4c35c-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

