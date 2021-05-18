---
title: PidTagAttachTag 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5a908b3543dff5cf011c9bd4d5d05b3a07004ead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361083"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="28edf-103">PidTagAttachTag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="28edf-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="28edf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28edf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28edf-105">添付ファイルを指定したアプリケーションを指定する ASN.1 オブジェクト識別子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="28edf-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28edf-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="28edf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="28edf-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="28edf-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="28edf-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="28edf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="28edf-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="28edf-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="28edf-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="28edf-110">Data type:</span></span>  <br/> |<span data-ttu-id="28edf-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="28edf-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="28edf-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="28edf-112">Area:</span></span>  <br/> |<span data-ttu-id="28edf-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="28edf-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28edf-114">注釈</span><span class="sxs-lookup"><span data-stu-id="28edf-114">Remarks</span></span>

<span data-ttu-id="28edf-115">このプロパティは、最初に添付ファイルを生成したアプリケーションを識別します。</span><span class="sxs-lookup"><span data-stu-id="28edf-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="28edf-116">**メモ** プロパティ **PR_ATTACH_ENCODING** [(PidTagAttachEncoding)](pidtagattachencoding-canonical-property.md)とPR_ATTACH_TAG **プロパティは** 混同しないでください。</span><span class="sxs-lookup"><span data-stu-id="28edf-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="28edf-117">これらはペアまたは関連付けではありません。</span><span class="sxs-lookup"><span data-stu-id="28edf-117">They are not paired or related.</span></span> <span data-ttu-id="28edf-118">**PR_ATTACH_ENCODING、** 添付ファイル内のデータを変換するために使用されるアルゴリズムを識別します。</span><span class="sxs-lookup"><span data-stu-id="28edf-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="28edf-119">"Object" はオブジェクト識別子という用語で、X.400 使用法ではオブジェクト指向プログラミングよりもずっと一般的な意味を持ちます。</span><span class="sxs-lookup"><span data-stu-id="28edf-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="28edf-120">オブジェクト識別子の構文とサンプル オブジェクト識別子は、MAPIOID で定義されます。H ヘッダー ファイル。</span><span class="sxs-lookup"><span data-stu-id="28edf-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="28edf-121">値は **PR_ATTACH_TAG** MAPIOID.H で定義されている値に限定されません。</span><span class="sxs-lookup"><span data-stu-id="28edf-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="28edf-122">これらのオブジェクト識別子の詳細については、ASN.1、X.208、X.209 のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="28edf-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="28edf-123">オブジェクト識別子は、ファイル転送本文パーツ (FTBP) 環境のアプリケーション参照要素に含まれる。</span><span class="sxs-lookup"><span data-stu-id="28edf-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="28edf-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="28edf-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="28edf-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="28edf-125">Protocol specifications</span></span>

<span data-ttu-id="28edf-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28edf-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28edf-127">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="28edf-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="28edf-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="28edf-128">Header files</span></span>

<span data-ttu-id="28edf-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28edf-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="28edf-130">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="28edf-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="28edf-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="28edf-131">Mapitags.h</span></span>
  
> <span data-ttu-id="28edf-132">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="28edf-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28edf-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="28edf-133">See also</span></span>



[<span data-ttu-id="28edf-134">PidTagAttachMimeTag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="28edf-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="28edf-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="28edf-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="28edf-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="28edf-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="28edf-137">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="28edf-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="28edf-138">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="28edf-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

