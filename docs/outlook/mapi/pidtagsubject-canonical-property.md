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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339257"
---
# <a name="pidtagsubject-canonical-property"></a><span data-ttu-id="e5a08-103">PidTagSubject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e5a08-103">PidTagSubject Canonical Property</span></span>

  
  
<span data-ttu-id="e5a08-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5a08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5a08-105">メッセージの完全な件名を含みます。</span><span class="sxs-lookup"><span data-stu-id="e5a08-105">Contains the full subject of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5a08-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e5a08-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e5a08-107">PR_SUBJECT、PR_SUBJECT_A、PR_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="e5a08-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="e5a08-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e5a08-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e5a08-109">0x0037</span><span class="sxs-lookup"><span data-stu-id="e5a08-109">0x0037</span></span>  <br/> |
|<span data-ttu-id="e5a08-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e5a08-110">Data type:</span></span>  <br/> |<span data-ttu-id="e5a08-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e5a08-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e5a08-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e5a08-112">Area:</span></span>  <br/> |<span data-ttu-id="e5a08-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="e5a08-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5a08-114">解説</span><span class="sxs-lookup"><span data-stu-id="e5a08-114">Remarks</span></span>

<span data-ttu-id="e5a08-115">これらのプロパティは、すべてのメッセージオブジェクトで推奨されます。</span><span class="sxs-lookup"><span data-stu-id="e5a08-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="e5a08-116">これらのプロパティは常に、完全な件名のテキスト (プレフィックスと正規化された件名の連結) です。</span><span class="sxs-lookup"><span data-stu-id="e5a08-116">These properties are always the full subject text, that is, the concatenation of the prefix and the normalized subject.</span></span> <span data-ttu-id="e5a08-117">プレフィックスがない場合は、正規化された件名を件名と同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5a08-117">If there is no prefix, the normalized subject should be the same as the subject.</span></span> <span data-ttu-id="e5a08-118">メッセージストアまたはトランスポートプロバイダーは、これらのプロパティと**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) プロパティの両方を使用して、 **PR_NORMALIZED_SUBJECT**に記述されている規則を使用して正規化されたサブジェクトを計算します ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5a08-118">A message store or transport provider uses both these properties and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties to compute the normalized subject using the rule described under **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span></span>
  
<span data-ttu-id="e5a08-119">件名のプロパティは通常、256文字未満の小さな文字列で、メッセージストアプロバイダーは、それらの**IStream**インターフェイスをサポートする義務がありません。</span><span class="sxs-lookup"><span data-stu-id="e5a08-119">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the **IStream** interface on them.</span></span> <span data-ttu-id="e5a08-120">クライアントは、常に**imapiprop**インターフェイスを使用してアクセスを試行し、 **MAPI_E_NOT_ENOUGH_MEMORY**が返された場合にのみ**IStream**に頼る必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5a08-120">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
<span data-ttu-id="e5a08-121">レポートの場合、このプロパティには、メッセージに対して発生したことを示す文字列が前にある、元のメッセージの件名が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e5a08-121">For a report, this property contains the original message's subject preceded by a string indicating what has happened to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e5a08-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e5a08-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e5a08-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e5a08-123">Protocol specifications</span></span>

<span data-ttu-id="e5a08-124">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5a08-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5a08-125">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e5a08-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e5a08-126">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5a08-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5a08-127">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="e5a08-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e5a08-128">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e5a08-128">Header files</span></span>

<span data-ttu-id="e5a08-129">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5a08-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="e5a08-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e5a08-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="e5a08-131">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e5a08-131">Mapitags.h</span></span>
  
> <span data-ttu-id="e5a08-132">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e5a08-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5a08-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5a08-133">See also</span></span>



[<span data-ttu-id="e5a08-134">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e5a08-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e5a08-135">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e5a08-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e5a08-136">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e5a08-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e5a08-137">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e5a08-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

