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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 53ee4019752cf717840199d4a51cbc90133b8636
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320392"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="48d01-103">PidTagUserCertificate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="48d01-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="48d01-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48d01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48d01-105">メッセージング ユーザーの ASN.1 認証証明書が含まれる。</span><span class="sxs-lookup"><span data-stu-id="48d01-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48d01-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="48d01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48d01-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="48d01-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="48d01-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="48d01-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48d01-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="48d01-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="48d01-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="48d01-110">Data type:</span></span>  <br/> |<span data-ttu-id="48d01-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="48d01-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="48d01-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="48d01-112">Area:</span></span>  <br/> |<span data-ttu-id="48d01-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="48d01-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48d01-114">注釈</span><span class="sxs-lookup"><span data-stu-id="48d01-114">Remarks</span></span>

<span data-ttu-id="48d01-115">認証証明書はデジタル署名に似ています。</span><span class="sxs-lookup"><span data-stu-id="48d01-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="48d01-116">複数の MAPI プロパティは、ASN.1 証明書を提供します。</span><span class="sxs-lookup"><span data-stu-id="48d01-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="48d01-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="48d01-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48d01-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="48d01-118">Protocol specifications</span></span>

<span data-ttu-id="48d01-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48d01-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48d01-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="48d01-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="48d01-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48d01-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48d01-122">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="48d01-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48d01-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="48d01-123">Header files</span></span>

<span data-ttu-id="48d01-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48d01-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="48d01-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="48d01-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="48d01-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48d01-126">Mapitags.h</span></span>
  
> <span data-ttu-id="48d01-127">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="48d01-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48d01-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="48d01-128">See also</span></span>



[<span data-ttu-id="48d01-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="48d01-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48d01-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="48d01-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48d01-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="48d01-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48d01-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="48d01-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

