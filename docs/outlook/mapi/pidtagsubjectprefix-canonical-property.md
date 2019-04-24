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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339229"
---
# <a name="pidtagsubjectprefix-canonical-property"></a><span data-ttu-id="c410e-103">PidTagSubjectPrefix 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c410e-103">PidTagSubjectPrefix Canonical Property</span></span>

  
  
<span data-ttu-id="c410e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c410e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c410e-105">通常、メッセージに何らかのアクション (転送の場合は "FW:" など) を示す件名のプレフィックスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c410e-105">Contains a subject prefix that typically indicates some action on a message, such as "FW: " for forwarding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c410e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c410e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c410e-107">PR_SUBJECT_PREFIX、PR_SUBJECT_PREFIX_A、PR_SUBJECT_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="c410e-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="c410e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c410e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c410e-109">0x003d</span><span class="sxs-lookup"><span data-stu-id="c410e-109">0x003D</span></span>  <br/> |
|<span data-ttu-id="c410e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c410e-110">Data type:</span></span>  <br/> |<span data-ttu-id="c410e-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c410e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c410e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c410e-112">Area:</span></span>  <br/> |<span data-ttu-id="c410e-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="c410e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c410e-114">解説</span><span class="sxs-lookup"><span data-stu-id="c410e-114">Remarks</span></span>

<span data-ttu-id="c410e-115">これらのプロパティは、すべてのメッセージオブジェクトで推奨されます。</span><span class="sxs-lookup"><span data-stu-id="c410e-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="c410e-116">件名のプレフィックスは、1つ以上の英数字で構成され、その後にコロンとスペース (プレフィックスの一部) が続きます。</span><span class="sxs-lookup"><span data-stu-id="c410e-116">The subject prefix consists of one or more alphanumeric characters, followed by a colon and a space (which are part of the prefix).</span></span> <span data-ttu-id="c410e-117">コロンの前に英数字以外の文字を含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="c410e-117">It must not contain any nonalphanumeric characters before the colon.</span></span> <span data-ttu-id="c410e-118">プレフィックスを指定しない場合は、空の文字列、またはこのプロパティが設定されていないことがあります。</span><span class="sxs-lookup"><span data-stu-id="c410e-118">Absence of a prefix can be represented by an empty string or by this property not being set.</span></span> 
  
<span data-ttu-id="c410e-119">これらのプロパティが明示的に設定されている場合、文字列の長さは任意で、任意の英数字を使用できますが、 **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティの先頭にある部分文字列に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c410e-119">If these properties are set explicitly, the string can be of any length and use any alphanumeric characters, but it must match a substring at the beginning of the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="c410e-120">これらのプロパティが送信者によって設定されておらず、計算する必要がある場合、そのコンテンツはより制限されます。</span><span class="sxs-lookup"><span data-stu-id="c410e-120">If these properties are not set by the sender and must be computed, their contents are more restricted.</span></span> <span data-ttu-id="c410e-121">プレフィックスを計算する規則は、 **PR_SUBJECT**が1、2、または3文字 (アルファベットのみ) で始まり、その後にコロンとスペースが続く必要があるということです。</span><span class="sxs-lookup"><span data-stu-id="c410e-121">The rule for computing the prefix is that **PR_SUBJECT** must begin with one, two, or three letters (alphabetic only) followed by a colon and a space.</span></span> <span data-ttu-id="c410e-122">このようなサブ文字列が**PR_SUBJECT**の先頭にある場合は、これらのプロパティの文字列になります (また、 **PR_SUBJECT**の先頭にも留まりません)。</span><span class="sxs-lookup"><span data-stu-id="c410e-122">If such a substring is found at the beginning of **PR_SUBJECT**, it then becomes the string for these properties (and also stays at the beginning of **PR_SUBJECT**).</span></span> <span data-ttu-id="c410e-123">それ以外の場合、これらのプロパティは未設定のままです。</span><span class="sxs-lookup"><span data-stu-id="c410e-123">Otherwise, these properties remain unset.</span></span> 
  
<span data-ttu-id="c410e-124">これらのプロパティと**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) は、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)実装の一部として計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c410e-124">These properties and **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="c410e-125">クライアントは、imapiprop: **: SaveChanges**呼び出しでコミットされるまで、値に対して[imapiprop:: GetProps](imapiprop-getprops.md)にプロンプトを表示しません。</span><span class="sxs-lookup"><span data-stu-id="c410e-125">A client should not prompt [IMAPIProp::GetProps](imapiprop-getprops.md) for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="c410e-126">件名のプロパティは通常、256文字未満の小さな文字列で、メッセージストアプロバイダーは、それらの OLE **IStream**インターフェイスをサポートする義務がありません。</span><span class="sxs-lookup"><span data-stu-id="c410e-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the OLE **IStream** interface on them.</span></span> <span data-ttu-id="c410e-127">クライアントは、常に**imapiprop**インターフェイスを使用してアクセスを試行し、 **MAPI_E_NOT_ENOUGH_MEMORY**が返された場合にのみ**IStream**に頼る必要があります。</span><span class="sxs-lookup"><span data-stu-id="c410e-127">A client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c410e-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c410e-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c410e-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c410e-129">Protocol specifications</span></span>

<span data-ttu-id="c410e-130">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c410e-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c410e-131">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c410e-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c410e-132">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c410e-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c410e-133">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="c410e-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="c410e-134">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c410e-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c410e-135">電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c410e-135">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c410e-136">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c410e-136">Header files</span></span>

<span data-ttu-id="c410e-137">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c410e-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="c410e-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c410e-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="c410e-139">Mapitags</span><span class="sxs-lookup"><span data-stu-id="c410e-139">Mapitags.h</span></span>
  
> <span data-ttu-id="c410e-140">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c410e-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c410e-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="c410e-141">See also</span></span>



[<span data-ttu-id="c410e-142">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c410e-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c410e-143">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c410e-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c410e-144">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c410e-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c410e-145">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c410e-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

