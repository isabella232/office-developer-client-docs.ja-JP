---
title: PidTagNormalizedSubject 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 54a0f438dacc8a1c7838eb538ec05c5c263f1b0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329275"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a><span data-ttu-id="ee6a7-103">PidTagNormalizedSubject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ee6a7-103">PidTagNormalizedSubject Canonical Property</span></span>

  
  
<span data-ttu-id="ee6a7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee6a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee6a7-105">プレフィックスが削除されたメッセージの件名が含まれる。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-105">Contains the message subject with any prefix removed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee6a7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ee6a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee6a7-107">PR_NORMALIZED_SUBJECT、PR_NORMALIZED_SUBJECT_A、PR_NORMALIZED_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="ee6a7-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="ee6a7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ee6a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee6a7-109">0x0E1D</span><span class="sxs-lookup"><span data-stu-id="ee6a7-109">0x0E1D</span></span>  <br/> |
|<span data-ttu-id="ee6a7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ee6a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee6a7-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ee6a7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ee6a7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ee6a7-112">Area:</span></span>  <br/> |<span data-ttu-id="ee6a7-113">メール</span><span class="sxs-lookup"><span data-stu-id="ee6a7-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee6a7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ee6a7-114">Remarks</span></span>

<span data-ttu-id="ee6a7-115">これらのプロパティは **、PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティおよび **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) プロパティのメッセージ ストアまたはトランスポート プロバイダーによって次のように計算されます。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-115">These properties are computed by message store or transport providers from the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties in the following manner.</span></span>
  
- <span data-ttu-id="ee6a7-116">PR_SUBJECT_PREFIXが存在 **し\*\*\*\*、PR_SUBJECT** の初期部分文字列である場合 **、PR_NORMALIZED_SUBJECT** と関連付けられたプロパティは、プレフィックスが削除された PR_SUBJECT の内容 **に** 設定されます。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-116">If the **PR_SUBJECT_PREFIX** is present and is an initial substring of **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** and associated properties are set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
- <span data-ttu-id="ee6a7-117">**PR_SUBJECT_PREFIX** が存在するが、PR_SUBJECT の初期部分文字列ではない場合、PR_SUBJECT_PREFIX は次のルールを使用して PR_SUBJECT から削除および再計算されます。PR_SUBJECT に含まれる文字列が 1 ~ **3** 文字の非数値文字の後にコロンとスペースが続く場合は、コロンとブランクと共に文字列がプレフィックスになります。 </span><span class="sxs-lookup"><span data-stu-id="ee6a7-117">If **PR_SUBJECT_PREFIX** is present, but it is not an initial substring of **PR_SUBJECT**, **PR_SUBJECT_PREFIX** is deleted and recalculated from **PR_SUBJECT** using the following rule: If the string contained in **PR_SUBJECT** begins with one to three non-numeric characters followed by a colon and a space, then the string together with the colon and the blank becomes the prefix.</span></span> <span data-ttu-id="ee6a7-118">数字、空白文字、句読点文字は、有効なプレフィックス文字ではありません。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-118">Numbers, blanks, and punctuation characters are not valid prefix characters.</span></span> 
    
- <span data-ttu-id="ee6a7-119">この **PR_SUBJECT_PREFIX** が存在しない場合は、前の手順で **PR_SUBJECTを使用** して計算されます。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-119">If **PR_SUBJECT_PREFIX** is not present, it is calculated from **PR_SUBJECT** using the rule outlined in the previous step.</span></span> <span data-ttu-id="ee6a7-120">このプロパティは、プレフィックスが削除されたPR_SUBJECT **の内容** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-120">This property then is set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
 <span data-ttu-id="ee6a7-121">**メモ** 指定 **PR_SUBJECT_PREFIX** 文字列の場合、PR_SUBJECT **プロパティは** 同じです。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-121">**Note** When **PR_SUBJECT_PREFIX** is an empty string, **PR_SUBJECT** and this property are the same.</span></span> 
  
<span data-ttu-id="ee6a7-122">最終的には、このプロパティはプレフィックスの **後PR_SUBJECT部分** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-122">Ultimately, this property should be the part of **PR_SUBJECT** following the prefix.</span></span> <span data-ttu-id="ee6a7-123">プレフィックスがない場合、このプロパティは次のプロパティと **同PR_SUBJECT。**</span><span class="sxs-lookup"><span data-stu-id="ee6a7-123">If there is no prefix, this property becomes the same as **PR_SUBJECT**.</span></span>
  
 <span data-ttu-id="ee6a7-124">**PR_SUBJECT_PREFIX** このプロパティは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) 実装の一部として計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-124">**PR_SUBJECT_PREFIX** and this property should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="ee6a7-125">クライアント アプリケーションは [、IMAPIProp::SaveChanges](imapiprop-getprops.md) 呼び出しによってコミットされるまで **、IMAPIProp::GetProps** メソッドの値を求める必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-125">A client application should not prompt the [IMAPIProp::GetProps](imapiprop-getprops.md) method for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="ee6a7-126">件名プロパティは、通常、256 文字未満の小さな文字列であり、メッセージ ストア プロバイダーは、オブジェクト リンクおよび埋め込み (OLE) **IStream** インターフェイスをサポートする義務はありません。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="ee6a7-127">クライアントは、必ず最初に **IMAPIProp** インターフェイスを介してアクセスを試行し **、IStream** にアクセスMAPI_E_NOT_ENOUGH_MEMORY必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-127">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if MAPI_E_NOT_ENOUGH_MEMORY is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ee6a7-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ee6a7-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ee6a7-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ee6a7-129">Protocol specifications</span></span>

<span data-ttu-id="ee6a7-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee6a7-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee6a7-131">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ee6a7-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee6a7-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee6a7-133">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="ee6a7-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee6a7-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee6a7-135">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ee6a7-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ee6a7-136">Header files</span></span>

<span data-ttu-id="ee6a7-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee6a7-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee6a7-138">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="ee6a7-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ee6a7-139">Mapitags.h</span></span>
  
> <span data-ttu-id="ee6a7-140">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="ee6a7-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee6a7-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee6a7-141">See also</span></span>



[<span data-ttu-id="ee6a7-142">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ee6a7-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee6a7-143">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ee6a7-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee6a7-144">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ee6a7-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee6a7-145">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ee6a7-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

