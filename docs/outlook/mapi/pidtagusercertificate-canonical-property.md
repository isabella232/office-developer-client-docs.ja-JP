---
title: PidTagUserCertificate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserCertificate
api_type:
- COM
ms.assetid: 2ac14c43-36c1-4f2f-97b0-2462f2360575
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0dd477a055562f692c8869bc436c4238c77fd02a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803661"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="ce98b-103">PidTagUserCertificate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ce98b-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="ce98b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce98b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ce98b-105">ASN.1 にメッセージングのユーザーの認証証明書が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ce98b-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce98b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ce98b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ce98b-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="ce98b-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="ce98b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ce98b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ce98b-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="ce98b-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="ce98b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ce98b-110">Data type:</span></span>  <br/> |<span data-ttu-id="ce98b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ce98b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ce98b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ce98b-112">Area:</span></span>  <br/> |<span data-ttu-id="ce98b-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="ce98b-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce98b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ce98b-114">Remarks</span></span>

<span data-ttu-id="ce98b-115">認証の証明書は、デジタル署名に似ています。</span><span class="sxs-lookup"><span data-stu-id="ce98b-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="ce98b-116">いくつかの MAPI プロパティでは、ASN.1 の証明書を提供します。</span><span class="sxs-lookup"><span data-stu-id="ce98b-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ce98b-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ce98b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ce98b-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ce98b-118">Protocol specifications</span></span>

<span data-ttu-id="ce98b-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce98b-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ce98b-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ce98b-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ce98b-121">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce98b-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ce98b-122">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ce98b-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ce98b-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ce98b-123">Header files</span></span>

<span data-ttu-id="ce98b-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ce98b-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="ce98b-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ce98b-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="ce98b-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ce98b-126">Mapitags.h</span></span>
  
> <span data-ttu-id="ce98b-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ce98b-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ce98b-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="ce98b-128">See also</span></span>



[<span data-ttu-id="ce98b-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ce98b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ce98b-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ce98b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ce98b-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ce98b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ce98b-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ce98b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

