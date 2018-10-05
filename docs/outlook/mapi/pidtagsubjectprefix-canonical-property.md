---
title: PidTagSubjectPrefix 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385649"
---
# <a name="pidtagsubjectprefix-canonical-property"></a><span data-ttu-id="9bfad-103">PidTagSubjectPrefix 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9bfad-103">PidTagSubjectPrefix Canonical Property</span></span>

  
  
<span data-ttu-id="9bfad-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bfad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bfad-105">通常次のように、メッセージのいくつかのアクションを示す件名のプレフィックスが含まれています"FW:"転送します。</span><span class="sxs-lookup"><span data-stu-id="9bfad-105">Contains a subject prefix that typically indicates some action on a message, such as "FW: " for forwarding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9bfad-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9bfad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9bfad-107">されて、PR_SUBJECT_PREFIX_A、PR_SUBJECT_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="9bfad-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="9bfad-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9bfad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9bfad-109">0x003D</span><span class="sxs-lookup"><span data-stu-id="9bfad-109">0x003D</span></span>  <br/> |
|<span data-ttu-id="9bfad-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9bfad-110">Data type:</span></span>  <br/> |<span data-ttu-id="9bfad-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9bfad-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9bfad-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9bfad-112">Area:</span></span>  <br/> |<span data-ttu-id="9bfad-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="9bfad-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bfad-114">備考</span><span class="sxs-lookup"><span data-stu-id="9bfad-114">Remarks</span></span>

<span data-ttu-id="9bfad-115">これらのプロパティは、すべてのメッセージ オブジェクトに対して推奨されています。</span><span class="sxs-lookup"><span data-stu-id="9bfad-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="9bfad-116">件名のプレフィックスは、1 つまたは複数文字の英数字、続いてコロンとスペース (これは、プレフィックスの一部である) で構成されています。</span><span class="sxs-lookup"><span data-stu-id="9bfad-116">The subject prefix consists of one or more alphanumeric characters, followed by a colon and a space (which are part of the prefix).</span></span> <span data-ttu-id="9bfad-117">コロンの前に任意の英数字以外の文字が含まれていない必要があります。</span><span class="sxs-lookup"><span data-stu-id="9bfad-117">It must not contain any nonalphanumeric characters before the colon.</span></span> <span data-ttu-id="9bfad-118">プレフィックスがない場合は、このプロパティが設定されていない、空の文字列で表現できます。</span><span class="sxs-lookup"><span data-stu-id="9bfad-118">Absence of a prefix can be represented by an empty string or by this property not being set.</span></span> 
  
<span data-ttu-id="9bfad-119">これらのプロパティは、明示的に設定されている場合は文字列は任意の長さにして、任意の英数字を使用が、**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティの先頭の部分文字列に一致しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9bfad-119">If these properties are set explicitly, the string can be of any length and use any alphanumeric characters, but it must match a substring at the beginning of the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="9bfad-120">これらのプロパティでは、送信者が設定されていないと、計算する必要がある場合、その内容より制限されています。</span><span class="sxs-lookup"><span data-stu-id="9bfad-120">If these properties are not set by the sender and must be computed, their contents are more restricted.</span></span> <span data-ttu-id="9bfad-121">接頭辞を計算するためのルールは、**あるの PR_SUBJECT**が 1、2、または 3 文字で始まる必要があります (アルファベットのみ)、コロンとスペースの後にします。</span><span class="sxs-lookup"><span data-stu-id="9bfad-121">The rule for computing the prefix is that **PR_SUBJECT** must begin with one, two, or three letters (alphabetic only) followed by a colon and a space.</span></span> <span data-ttu-id="9bfad-122">このような部分が**あるの PR_SUBJECT**の先頭にある場合、これらのプロパティの文字列になります (および**あるの PR_SUBJECT**の先頭のままでも)。</span><span class="sxs-lookup"><span data-stu-id="9bfad-122">If such a substring is found at the beginning of **PR_SUBJECT**, it then becomes the string for these properties (and also stays at the beginning of **PR_SUBJECT**).</span></span> <span data-ttu-id="9bfad-123">それ以外の場合、これらのプロパティは設定されていないままです。</span><span class="sxs-lookup"><span data-stu-id="9bfad-123">Otherwise, these properties remain unset.</span></span> 
  
<span data-ttu-id="9bfad-124">これらのプロパティと**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)の実装の一部として計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9bfad-124">These properties and **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="9bfad-125">クライアントは、いない、コミットされた後になるまでの値の[IMAPIProp::GetProps](imapiprop-getprops.md)を促す必要がある**IMAPIProp::SaveChanges**の呼び出しによって、です。</span><span class="sxs-lookup"><span data-stu-id="9bfad-125">A client should not prompt [IMAPIProp::GetProps](imapiprop-getprops.md) for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="9bfad-126">256 文字は、通常は短い文字列は、件名のプロパティと、メッセージ ストア プロバイダーがこれらの OLE **IStream**インターフェイスをサポートするために義務を負いません。</span><span class="sxs-lookup"><span data-stu-id="9bfad-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the OLE **IStream** interface on them.</span></span> <span data-ttu-id="9bfad-127">クライアントは、 **IMAPIProp**インターフェイスを介してアクセスを最初に試行し、 **MAPI_E_NOT_ENOUGH_MEMORY**が返された場合にのみ、 **IStream**に頼る必要があります常に。</span><span class="sxs-lookup"><span data-stu-id="9bfad-127">A client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9bfad-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9bfad-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9bfad-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9bfad-129">Protocol specifications</span></span>

<span data-ttu-id="9bfad-130">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bfad-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bfad-131">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9bfad-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9bfad-132">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bfad-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bfad-133">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="9bfad-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9bfad-134">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bfad-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bfad-135">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9bfad-135">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9bfad-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9bfad-136">Header files</span></span>

<span data-ttu-id="9bfad-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9bfad-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="9bfad-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9bfad-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="9bfad-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9bfad-139">Mapitags.h</span></span>
  
> <span data-ttu-id="9bfad-140">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9bfad-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9bfad-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="9bfad-141">See also</span></span>



[<span data-ttu-id="9bfad-142">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9bfad-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9bfad-143">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9bfad-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9bfad-144">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9bfad-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9bfad-145">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9bfad-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

