---
title: PidTagOriginalSubject 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubject
api_type:
- COM
ms.assetid: 8668ba4f-3236-4a87-a5aa-9cf7eea3d87b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cf81a5b4c10cb7bff5f03a1b25d11bbaa8ff277
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803102"
---
# <a name="pidtagoriginalsubject-canonical-property"></a><span data-ttu-id="35bc6-103">PidTagOriginalSubject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="35bc6-103">PidTagOriginalSubject Canonical Property</span></span>

  
  
<span data-ttu-id="35bc6-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35bc6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35bc6-105">メッセージに関するレポートで使用するための元のメッセージの件名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="35bc6-105">Contains the subject of an original message for use in a report about the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35bc6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="35bc6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35bc6-107">PR_ORIGINAL_SUBJECT、PR_ORIGINAL_SUBJECT_A、PR_ORIGINAL_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="35bc6-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="35bc6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="35bc6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35bc6-109">0x0049</span><span class="sxs-lookup"><span data-stu-id="35bc6-109">0x0049</span></span>  <br/> |
|<span data-ttu-id="35bc6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="35bc6-110">Data type:</span></span>  <br/> |<span data-ttu-id="35bc6-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="35bc6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="35bc6-112">領域:</span><span class="sxs-lookup"><span data-stu-id="35bc6-112">Area:</span></span>  <br/> |<span data-ttu-id="35bc6-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="35bc6-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35bc6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="35bc6-114">Remarks</span></span>

<span data-ttu-id="35bc6-115">**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) のプロパティと同じ値には、これらのプロパティは設定されました。</span><span class="sxs-lookup"><span data-stu-id="35bc6-115">These properties are originally set to the same value as the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="35bc6-116">256 文字は、通常は短い文字列は、件名のプロパティと、メッセージ ストア プロバイダーがそれらのオブジェクトのリンクと埋め込み (OLE) の**IStream**インターフェイスをサポートする義務を負いません。</span><span class="sxs-lookup"><span data-stu-id="35bc6-116">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="35bc6-117">クライアントは、 **IMAPIProp**インターフェイスを介してアクセスを最初に試行し、 **MAPI_E_NOT_ENOUGH_MEMORY**が返された場合にのみ、 **IStream**に頼る必要があります常に。</span><span class="sxs-lookup"><span data-stu-id="35bc6-117">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="35bc6-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="35bc6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="35bc6-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="35bc6-119">Protocol specifications</span></span>

<span data-ttu-id="35bc6-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35bc6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35bc6-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="35bc6-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="35bc6-122">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35bc6-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35bc6-123">サーバーとクライアントの間のメッセージングのオブジェクト データの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="35bc6-123">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="35bc6-124">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35bc6-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35bc6-125">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="35bc6-125">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="35bc6-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="35bc6-126">Header files</span></span>

<span data-ttu-id="35bc6-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35bc6-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="35bc6-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="35bc6-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="35bc6-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="35bc6-129">Mapitags.h</span></span>
  
> <span data-ttu-id="35bc6-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="35bc6-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35bc6-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="35bc6-131">See also</span></span>



[<span data-ttu-id="35bc6-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="35bc6-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35bc6-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="35bc6-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35bc6-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="35bc6-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35bc6-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="35bc6-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

