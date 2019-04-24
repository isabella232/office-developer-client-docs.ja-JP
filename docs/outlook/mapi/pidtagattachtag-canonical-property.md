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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5a908b3543dff5cf011c9bd4d5d05b3a07004ead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361083"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="e9620-103">PidTagAttachTag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9620-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="e9620-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9620-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9620-105">添付ファイルを提供したアプリケーションを指定する、ASN. 1 つのオブジェクト識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="e9620-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9620-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e9620-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9620-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="e9620-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="e9620-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e9620-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9620-109">0x370a</span><span class="sxs-lookup"><span data-stu-id="e9620-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="e9620-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e9620-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9620-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e9620-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e9620-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e9620-112">Area:</span></span>  <br/> |<span data-ttu-id="e9620-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="e9620-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9620-114">解説</span><span class="sxs-lookup"><span data-stu-id="e9620-114">Remarks</span></span>

<span data-ttu-id="e9620-115">このプロパティは、添付ファイルを最初に生成したアプリケーションを識別します。</span><span class="sxs-lookup"><span data-stu-id="e9620-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="e9620-116">**メモ\*\*\*\*PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) および**PR_ATTACH_TAG**プロパティは、混同しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="e9620-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="e9620-117">ペアになっていないか、関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="e9620-117">They are not paired or related.</span></span> <span data-ttu-id="e9620-118">**PR_ATTACH_ENCODING**添付ファイル内のデータの変換に使用するアルゴリズムを指定します。</span><span class="sxs-lookup"><span data-stu-id="e9620-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="e9620-119">"object" は、用語オブジェクトの識別子、およびオブジェクト指向プログラミングの場合よりも、X の使用法でより一般的な意味を持ちます。</span><span class="sxs-lookup"><span data-stu-id="e9620-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="e9620-120">オブジェクト識別子の構文とサンプルオブジェクトの識別子は、MAPIOID で定義されています。H ヘッダーファイル。</span><span class="sxs-lookup"><span data-stu-id="e9620-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="e9620-121">**PR_ATTACH_TAG**の値は、MAPIOID で定義されている値に限定されません。H.</span><span class="sxs-lookup"><span data-stu-id="e9620-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="e9620-122">これらのオブジェクト識別子の詳細については、209個のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9620-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="e9620-123">オブジェクト識別子は、ファイル転送本文パーツ (ftbp) 環境のアプリケーション参照要素にあります。</span><span class="sxs-lookup"><span data-stu-id="e9620-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e9620-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e9620-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9620-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e9620-125">Protocol specifications</span></span>

<span data-ttu-id="e9620-126">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9620-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9620-127">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="e9620-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9620-128">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e9620-128">Header files</span></span>

<span data-ttu-id="e9620-129">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9620-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9620-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e9620-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9620-131">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e9620-131">Mapitags.h</span></span>
  
> <span data-ttu-id="e9620-132">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e9620-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9620-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9620-133">See also</span></span>



[<span data-ttu-id="e9620-134">PidTagAttachMimeTag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9620-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="e9620-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e9620-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9620-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9620-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9620-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e9620-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9620-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e9620-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

