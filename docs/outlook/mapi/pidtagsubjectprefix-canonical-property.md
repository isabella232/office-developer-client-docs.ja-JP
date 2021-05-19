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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339229"
---
# <a name="pidtagsubjectprefix-canonical-property"></a><span data-ttu-id="b9762-103">PidTagSubjectPrefix 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b9762-103">PidTagSubjectPrefix Canonical Property</span></span>

  
  
<span data-ttu-id="b9762-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9762-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9762-105">通常、メッセージに対する何らかのアクション (転送用の "FW:" など) を示す件名プレフィックスが含まれる。</span><span class="sxs-lookup"><span data-stu-id="b9762-105">Contains a subject prefix that typically indicates some action on a message, such as "FW: " for forwarding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b9762-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b9762-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9762-107">PR_SUBJECT_PREFIX、PR_SUBJECT_PREFIX_A、PR_SUBJECT_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="b9762-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="b9762-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b9762-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b9762-109">0x003D</span><span class="sxs-lookup"><span data-stu-id="b9762-109">0x003D</span></span>  <br/> |
|<span data-ttu-id="b9762-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b9762-110">Data type:</span></span>  <br/> |<span data-ttu-id="b9762-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b9762-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b9762-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b9762-112">Area:</span></span>  <br/> |<span data-ttu-id="b9762-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="b9762-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9762-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b9762-114">Remarks</span></span>

<span data-ttu-id="b9762-115">これらのプロパティは、すべてのメッセージ オブジェクトで推奨されます。</span><span class="sxs-lookup"><span data-stu-id="b9762-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="b9762-116">件名のプレフィックスは、1 つ以上の英数字で構成され、その後にコロンとスペース (プレフィックスの一部) が続きます。</span><span class="sxs-lookup"><span data-stu-id="b9762-116">The subject prefix consists of one or more alphanumeric characters, followed by a colon and a space (which are part of the prefix).</span></span> <span data-ttu-id="b9762-117">コロンの前に英数字以外の文字を含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="b9762-117">It must not contain any nonalphanumeric characters before the colon.</span></span> <span data-ttu-id="b9762-118">プレフィックスがない場合は、空の文字列で表したり、このプロパティを設定したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b9762-118">Absence of a prefix can be represented by an empty string or by this property not being set.</span></span> 
  
<span data-ttu-id="b9762-119">これらのプロパティが明示的に設定されている場合、文字列は任意の長さであり、任意の英数字を使用できますが **、PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティの先頭にある部分文字列と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9762-119">If these properties are set explicitly, the string can be of any length and use any alphanumeric characters, but it must match a substring at the beginning of the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="b9762-120">これらのプロパティが送信者によって設定されていないので、計算する必要がある場合、それらのプロパティの内容はさらに制限されます。</span><span class="sxs-lookup"><span data-stu-id="b9762-120">If these properties are not set by the sender and must be computed, their contents are more restricted.</span></span> <span data-ttu-id="b9762-121">プレフィックスを計算するルールは、PR_SUBJECT 1 文字、2 **文字、または** 3 文字 (アルファベットのみ) の後にコロンとスペースが続く必要がある点です。</span><span class="sxs-lookup"><span data-stu-id="b9762-121">The rule for computing the prefix is that **PR_SUBJECT** must begin with one, two, or three letters (alphabetic only) followed by a colon and a space.</span></span> <span data-ttu-id="b9762-122">このような部分文字列が PR_SUBJECT の先頭に見つかった場合は、これらのプロパティの文字列になります (また、これらのプロパティの先頭に **PR_SUBJECT)。**</span><span class="sxs-lookup"><span data-stu-id="b9762-122">If such a substring is found at the beginning of **PR_SUBJECT**, it then becomes the string for these properties (and also stays at the beginning of **PR_SUBJECT**).</span></span> <span data-ttu-id="b9762-123">それ以外の場合、これらのプロパティは未設定のままです。</span><span class="sxs-lookup"><span data-stu-id="b9762-123">Otherwise, these properties remain unset.</span></span> 
  
<span data-ttu-id="b9762-124">これらのプロパティと **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) は [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) 実装の一部として計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9762-124">These properties and **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="b9762-125">クライアントは [、IMAPIProp::SaveChanges](imapiprop-getprops.md) 呼び出しによってコミットされるまで **、IMAPIProp::GetProps** の値を求める必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9762-125">A client should not prompt [IMAPIProp::GetProps](imapiprop-getprops.md) for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="b9762-126">件名のプロパティは、通常、256 文字未満の小さな文字列であり、メッセージ ストア プロバイダーは、OLE **IStream** インターフェイスをサポートする義務はありません。</span><span class="sxs-lookup"><span data-stu-id="b9762-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the OLE **IStream** interface on them.</span></span> <span data-ttu-id="b9762-127">クライアントは常に最初に **IMAPIProp** インターフェイスを介してアクセスを試み **、IStream** にアクセス **MAPI_E_NOT_ENOUGH_MEMORY** 必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9762-127">A client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b9762-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b9762-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b9762-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b9762-129">Protocol specifications</span></span>

<span data-ttu-id="b9762-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9762-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9762-131">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="b9762-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b9762-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9762-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9762-133">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="b9762-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="b9762-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9762-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9762-135">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b9762-135">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b9762-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b9762-136">Header files</span></span>

<span data-ttu-id="b9762-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9762-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9762-138">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b9762-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="b9762-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b9762-139">Mapitags.h</span></span>
  
> <span data-ttu-id="b9762-140">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="b9762-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9762-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9762-141">See also</span></span>



[<span data-ttu-id="b9762-142">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b9762-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9762-143">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b9762-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9762-144">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b9762-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9762-145">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b9762-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

