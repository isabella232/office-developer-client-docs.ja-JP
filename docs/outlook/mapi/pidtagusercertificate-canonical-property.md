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
ms.openlocfilehash: 53ee4019752cf717840199d4a51cbc90133b8636
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320392"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="814a6-103">PidTagUserCertificate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="814a6-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="814a6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="814a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="814a6-105">メッセージングユーザーの ASN 認証証明書が保存されています。</span><span class="sxs-lookup"><span data-stu-id="814a6-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="814a6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="814a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="814a6-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="814a6-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="814a6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="814a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="814a6-109">0x3a22</span><span class="sxs-lookup"><span data-stu-id="814a6-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="814a6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="814a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="814a6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="814a6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="814a6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="814a6-112">Area:</span></span>  <br/> |<span data-ttu-id="814a6-113">MAPI メールユーザー</span><span class="sxs-lookup"><span data-stu-id="814a6-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="814a6-114">解説</span><span class="sxs-lookup"><span data-stu-id="814a6-114">Remarks</span></span>

<span data-ttu-id="814a6-115">認証証明書は、デジタル署名に似ています。</span><span class="sxs-lookup"><span data-stu-id="814a6-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="814a6-116">複数の MAPI プロパティで ASN. 1 証明書を指定します。</span><span class="sxs-lookup"><span data-stu-id="814a6-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="814a6-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="814a6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="814a6-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="814a6-118">Protocol specifications</span></span>

<span data-ttu-id="814a6-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="814a6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="814a6-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="814a6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="814a6-121">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="814a6-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="814a6-122">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="814a6-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="814a6-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="814a6-123">Header files</span></span>

<span data-ttu-id="814a6-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="814a6-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="814a6-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="814a6-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="814a6-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="814a6-126">Mapitags.h</span></span>
  
> <span data-ttu-id="814a6-127">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="814a6-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="814a6-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="814a6-128">See also</span></span>



[<span data-ttu-id="814a6-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="814a6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="814a6-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="814a6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="814a6-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="814a6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="814a6-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="814a6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

