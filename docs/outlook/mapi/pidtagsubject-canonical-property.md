---
title: PidTagSubject の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 63bb5534756f44aebd9e6ca21c336534b279909d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803611"
---
# <a name="pidtagsubject-canonical-property"></a><span data-ttu-id="7c177-103">PidTagSubject の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7c177-103">PidTagSubject Canonical Property</span></span>

  
  
<span data-ttu-id="7c177-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c177-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c177-105">全メッセージの件名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c177-105">Contains the full subject of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c177-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7c177-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c177-107">あるの PR_SUBJECT、PR_SUBJECT_A、PR_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="7c177-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="7c177-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7c177-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c177-109">0x0037</span><span class="sxs-lookup"><span data-stu-id="7c177-109">0x0037</span></span>  <br/> |
|<span data-ttu-id="7c177-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="7c177-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c177-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7c177-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7c177-112">領域:</span><span class="sxs-lookup"><span data-stu-id="7c177-112">Area:</span></span>  <br/> |<span data-ttu-id="7c177-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="7c177-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c177-114">備考</span><span class="sxs-lookup"><span data-stu-id="7c177-114">Remarks</span></span>

<span data-ttu-id="7c177-115">これらのプロパティは、すべてのメッセージ オブジェクトに対して推奨されています。</span><span class="sxs-lookup"><span data-stu-id="7c177-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="7c177-116">これらのプロパティは、常にフルの件名のテキストをプレフィックスと正規化された件名を連結したものでは、です。</span><span class="sxs-lookup"><span data-stu-id="7c177-116">These properties are always the full subject text, that is, the concatenation of the prefix and the normalized subject.</span></span> <span data-ttu-id="7c177-117">プレフィックスがない場合は、正規化された件名は、件名の場合と同じにします。</span><span class="sxs-lookup"><span data-stu-id="7c177-117">If there is no prefix, the normalized subject should be the same as the subject.</span></span> <span data-ttu-id="7c177-118">メッセージを保存またはトランスポートのこれらのプロパティとルールを使用する正規化された件名を計算するために**されて**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) のプロパティの両方は、 **PR_NORMALIZED_SUBJECT** ([で説明されているプロバイダーの使用PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="7c177-118">A message store or transport provider uses both these properties and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties to compute the normalized subject using the rule described under **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span></span>
  
<span data-ttu-id="7c177-119">256 文字は、通常は短い文字列は、件名のプロパティと、メッセージ ストア プロバイダーがそれらに**IStream**インターフェイスをサポートする義務を負いません。</span><span class="sxs-lookup"><span data-stu-id="7c177-119">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the **IStream** interface on them.</span></span> <span data-ttu-id="7c177-120">クライアントは、 **IMAPIProp**インターフェイスを介してアクセスを最初に試行し、 **MAPI_E_NOT_ENOUGH_MEMORY**が返された場合にのみ、 **IStream**に頼る必要があります常に。</span><span class="sxs-lookup"><span data-stu-id="7c177-120">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
<span data-ttu-id="7c177-121">レポートの場合は、このプロパティは、元のメッセージの件名の前に、メッセージに何が起こったかを示す文字列を含みます。</span><span class="sxs-lookup"><span data-stu-id="7c177-121">For a report, this property contains the original message's subject preceded by a string indicating what has happened to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7c177-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7c177-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c177-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7c177-123">Protocol specifications</span></span>

<span data-ttu-id="7c177-124">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c177-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c177-125">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7c177-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c177-126">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c177-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c177-127">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="7c177-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c177-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7c177-128">Header files</span></span>

<span data-ttu-id="7c177-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c177-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c177-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7c177-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c177-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7c177-131">Mapitags.h</span></span>
  
> <span data-ttu-id="7c177-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c177-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c177-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c177-133">See also</span></span>



[<span data-ttu-id="7c177-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7c177-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c177-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7c177-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c177-136">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7c177-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c177-137">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="7c177-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

