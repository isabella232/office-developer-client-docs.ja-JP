---
title: PidTagUserX509Certificate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d27ef47a3ba387ae2e7acbcefc75b07ddd794e80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803665"
---
# <a name="pidtaguserx509certificate-canonical-property"></a><span data-ttu-id="262f1-103">PidTagUserX509Certificate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="262f1-103">PidTagUserX509Certificate Canonical Property</span></span>

  
  
<span data-ttu-id="262f1-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="262f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="262f1-105">メッセージング ユーザーの X.509 version 3 のセキュリティ証明書が含まれています。</span><span class="sxs-lookup"><span data-stu-id="262f1-105">Contains X.509 version 3 security certificates for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="262f1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="262f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="262f1-107">PR_USER_X509_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="262f1-107">PR_USER_X509_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="262f1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="262f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="262f1-109">0x3A70</span><span class="sxs-lookup"><span data-stu-id="262f1-109">0x3A70</span></span>  <br/> |
|<span data-ttu-id="262f1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="262f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="262f1-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="262f1-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="262f1-112">領域:</span><span class="sxs-lookup"><span data-stu-id="262f1-112">Area:</span></span>  <br/> |<span data-ttu-id="262f1-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="262f1-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="262f1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="262f1-114">Remarks</span></span>

<span data-ttu-id="262f1-115">公開キー セキュリティを使用するアプリケーションでこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="262f1-115">This property is used by applications that utilize public-key security.</span></span> <span data-ttu-id="262f1-116">1 つまたは複数の X.509 のバージョンの 3 つのセキュリティ証明書のバイナリ表現を保持します。</span><span class="sxs-lookup"><span data-stu-id="262f1-116">It holds a binary representation of one or more X.509 version 3 security certificates.</span></span> 
  
<span data-ttu-id="262f1-117">さまざまなアプリケーションおよびクライアントは、独自のセキュリティ証明書のこのプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="262f1-117">Various applications and clients can use this property for their own security certificates.</span></span> <span data-ttu-id="262f1-118">X.509 データのバイナリ形式は、ベンダーの間で変更できます。</span><span class="sxs-lookup"><span data-stu-id="262f1-118">The binary format of the X.509 data can vary among vendors.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="262f1-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="262f1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="262f1-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="262f1-120">Protocol specifications</span></span>

<span data-ttu-id="262f1-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="262f1-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="262f1-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="262f1-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="262f1-123">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="262f1-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="262f1-124">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="262f1-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="262f1-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="262f1-125">Header files</span></span>

<span data-ttu-id="262f1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="262f1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="262f1-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="262f1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="262f1-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="262f1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="262f1-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="262f1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="262f1-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="262f1-130">See also</span></span>



[<span data-ttu-id="262f1-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="262f1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="262f1-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="262f1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="262f1-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="262f1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="262f1-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="262f1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

