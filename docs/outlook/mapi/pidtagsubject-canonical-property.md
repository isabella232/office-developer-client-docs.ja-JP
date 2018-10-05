---
title: PidTagSubject 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386307"
---
# <a name="pidtagsubject-canonical-property"></a><span data-ttu-id="1cd76-103">PidTagSubject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cd76-103">PidTagSubject Canonical Property</span></span>

  
  
<span data-ttu-id="1cd76-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cd76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cd76-105">全メッセージの件名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1cd76-105">Contains the full subject of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1cd76-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1cd76-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1cd76-107">あるの PR_SUBJECT、PR_SUBJECT_A、PR_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="1cd76-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="1cd76-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1cd76-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1cd76-109">0x0037</span><span class="sxs-lookup"><span data-stu-id="1cd76-109">0x0037</span></span>  <br/> |
|<span data-ttu-id="1cd76-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1cd76-110">Data type:</span></span>  <br/> |<span data-ttu-id="1cd76-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1cd76-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1cd76-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1cd76-112">Area:</span></span>  <br/> |<span data-ttu-id="1cd76-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="1cd76-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cd76-114">備考</span><span class="sxs-lookup"><span data-stu-id="1cd76-114">Remarks</span></span>

<span data-ttu-id="1cd76-115">これらのプロパティは、すべてのメッセージ オブジェクトに対して推奨されています。</span><span class="sxs-lookup"><span data-stu-id="1cd76-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="1cd76-116">これらのプロパティは、常にフルの件名のテキストをプレフィックスと正規化された件名を連結したものでは、です。</span><span class="sxs-lookup"><span data-stu-id="1cd76-116">These properties are always the full subject text, that is, the concatenation of the prefix and the normalized subject.</span></span> <span data-ttu-id="1cd76-117">プレフィックスがない場合は、正規化された件名は、件名の場合と同じにします。</span><span class="sxs-lookup"><span data-stu-id="1cd76-117">If there is no prefix, the normalized subject should be the same as the subject.</span></span> <span data-ttu-id="1cd76-118">メッセージを保存またはトランスポートのこれらのプロパティとルールを使用する正規化された件名を計算するために**されて**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) のプロパティの両方は、 **PR_NORMALIZED_SUBJECT** ([で説明されているプロバイダーの使用PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="1cd76-118">A message store or transport provider uses both these properties and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties to compute the normalized subject using the rule described under **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span></span>
  
<span data-ttu-id="1cd76-119">256 文字は、通常は短い文字列は、件名のプロパティと、メッセージ ストア プロバイダーがそれらに**IStream**インターフェイスをサポートする義務を負いません。</span><span class="sxs-lookup"><span data-stu-id="1cd76-119">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the **IStream** interface on them.</span></span> <span data-ttu-id="1cd76-120">クライアントは、 **IMAPIProp**インターフェイスを介してアクセスを最初に試行し、 **MAPI_E_NOT_ENOUGH_MEMORY**が返された場合にのみ、 **IStream**に頼る必要があります常に。</span><span class="sxs-lookup"><span data-stu-id="1cd76-120">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
<span data-ttu-id="1cd76-121">レポートの場合は、このプロパティは、元のメッセージの件名の前に、メッセージに何が起こったかを示す文字列を含みます。</span><span class="sxs-lookup"><span data-stu-id="1cd76-121">For a report, this property contains the original message's subject preceded by a string indicating what has happened to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1cd76-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1cd76-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1cd76-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1cd76-123">Protocol specifications</span></span>

<span data-ttu-id="1cd76-124">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cd76-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cd76-125">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1cd76-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1cd76-126">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cd76-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cd76-127">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="1cd76-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1cd76-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1cd76-128">Header files</span></span>

<span data-ttu-id="1cd76-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1cd76-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="1cd76-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1cd76-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="1cd76-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1cd76-131">Mapitags.h</span></span>
  
> <span data-ttu-id="1cd76-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1cd76-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1cd76-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="1cd76-133">See also</span></span>



[<span data-ttu-id="1cd76-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cd76-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1cd76-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cd76-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1cd76-136">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1cd76-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1cd76-137">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1cd76-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

