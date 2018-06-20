---
title: PidTagAttachTag の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d8d8d32bddb98e0ac180b0898478c67297980492
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802517"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="4ad78-103">PidTagAttachTag の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="4ad78-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="4ad78-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4ad78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4ad78-105">添付ファイルを提供するアプリケーションを指定する ASN.1 オブジェクト識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4ad78-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ad78-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="4ad78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ad78-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="4ad78-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="4ad78-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4ad78-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ad78-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="4ad78-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="4ad78-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="4ad78-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ad78-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4ad78-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4ad78-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4ad78-112">Area:</span></span>  <br/> |<span data-ttu-id="4ad78-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="4ad78-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ad78-114">備考</span><span class="sxs-lookup"><span data-stu-id="4ad78-114">Remarks</span></span>

<span data-ttu-id="4ad78-115">このプロパティは、最初の添付ファイルを生成したアプリケーションを識別します。</span><span class="sxs-lookup"><span data-stu-id="4ad78-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="4ad78-116">**メモ****PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) と**PR_ATTACH_TAG**のプロパティとは違います。</span><span class="sxs-lookup"><span data-stu-id="4ad78-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="4ad78-117">ペアにしたり、関連にはしないでください。</span><span class="sxs-lookup"><span data-stu-id="4ad78-117">They are not paired or related.</span></span> <span data-ttu-id="4ad78-118">**PR_ATTACH_ENCODING**では、添付ファイル内のデータを変換するためのアルゴリズムを識別します。</span><span class="sxs-lookup"><span data-stu-id="4ad78-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="4ad78-119">「オブジェクト」より一般的な意味では、用語のオブジェクト識別子、および X.400 の使用法よりオブジェクト指向プログラミング。</span><span class="sxs-lookup"><span data-stu-id="4ad78-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="4ad78-120">オブジェクトの識別子の構文と例のオブジェクト識別子は、MAPIOID で定義されます。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="4ad78-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="4ad78-121">**PR_ATTACH_TAG**の値は、MAPIOID で定義されている制限付きではありません。H.</span><span class="sxs-lookup"><span data-stu-id="4ad78-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="4ad78-122">これらのオブジェクト識別子の詳細については、ASN.1、X.208、X.209 のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ad78-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="4ad78-123">ファイル転送の本文パーツ (FTBP) 環境の要素の参照がアプリケーションのオブジェクト識別子が検索されます。</span><span class="sxs-lookup"><span data-stu-id="4ad78-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4ad78-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4ad78-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4ad78-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4ad78-125">Protocol specifications</span></span>

<span data-ttu-id="4ad78-126">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ad78-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ad78-127">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="4ad78-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4ad78-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4ad78-128">Header files</span></span>

<span data-ttu-id="4ad78-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ad78-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ad78-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4ad78-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ad78-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4ad78-131">Mapitags.h</span></span>
  
> <span data-ttu-id="4ad78-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4ad78-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ad78-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ad78-133">See also</span></span>



[<span data-ttu-id="4ad78-134">PidTagAttachMimeTag の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="4ad78-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="4ad78-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4ad78-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ad78-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4ad78-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ad78-137">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="4ad78-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ad78-138">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="4ad78-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

