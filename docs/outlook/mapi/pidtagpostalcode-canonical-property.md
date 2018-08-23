---
title: PidTagPostalCode 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPostalCode
api_type:
- COM
ms.assetid: dd8e04b3-8959-4df4-ba2c-f6371180929b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f2c4efc8f8c04229901f03fd01381d13127575a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589015"
---
# <a name="pidtagpostalcode-canonical-property"></a><span data-ttu-id="5aa3f-103">PidTagPostalCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5aa3f-103">PidTagPostalCode Canonical Property</span></span>

  
  
<span data-ttu-id="5aa3f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5aa3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5aa3f-105">受信者の郵便番号と住所の郵便番号コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5aa3f-105">Contains the postal code for the recipient's postal address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5aa3f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5aa3f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5aa3f-107">PR_POSTAL_CODE、PR_POSTAL_CODE_A、PR_POSTAL_CODE_W、PR_BUSINESS_ADDRESS_POSTAL_CODE、PR_BUSINESS_ADDRESS_POSTAL_CODE_A、PR_BUSINESS_ADDRESS_POSTAL_CODE_W</span><span class="sxs-lookup"><span data-stu-id="5aa3f-107">PR_POSTAL_CODE, PR_POSTAL_CODE_A, PR_POSTAL_CODE_W, PR_BUSINESS_ADDRESS_POSTAL_CODE, PR_BUSINESS_ADDRESS_POSTAL_CODE_A, PR_BUSINESS_ADDRESS_POSTAL_CODE_W</span></span>  <br/> |
|<span data-ttu-id="5aa3f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5aa3f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5aa3f-109">0x3A2A</span><span class="sxs-lookup"><span data-stu-id="5aa3f-109">0x3A2A</span></span>  <br/> |
|<span data-ttu-id="5aa3f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5aa3f-110">Data type:</span></span>  <br/> |<span data-ttu-id="5aa3f-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="5aa3f-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="5aa3f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5aa3f-112">Area:</span></span>  <br/> |<span data-ttu-id="5aa3f-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="5aa3f-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5aa3f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5aa3f-114">Remarks</span></span>

<span data-ttu-id="5aa3f-115">これらのプロパティでは、識別を提供し、受信者の情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="5aa3f-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="5aa3f-116">受信者とその構造によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="5aa3f-116">They are defined by the recipient and their organization.</span></span> 
  
<span data-ttu-id="5aa3f-117">郵便番号のコードは、受信者の国または地域に固有です。</span><span class="sxs-lookup"><span data-stu-id="5aa3f-117">The postal code is specific to the recipient's country/region.</span></span> <span data-ttu-id="5aa3f-118">アメリカ合衆国では、このプロパティは、郵便番号を含みます。</span><span class="sxs-lookup"><span data-stu-id="5aa3f-118">In the United States of America, this property contains the ZIP code.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5aa3f-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5aa3f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5aa3f-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5aa3f-120">Protocol specifications</span></span>

<span data-ttu-id="5aa3f-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5aa3f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5aa3f-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5aa3f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5aa3f-123">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5aa3f-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5aa3f-124">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5aa3f-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="5aa3f-125">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5aa3f-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5aa3f-126">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5aa3f-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5aa3f-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5aa3f-127">Header files</span></span>

<span data-ttu-id="5aa3f-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5aa3f-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5aa3f-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5aa3f-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="5aa3f-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5aa3f-130">Mapitags.h</span></span>
  
> <span data-ttu-id="5aa3f-131">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5aa3f-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5aa3f-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="5aa3f-132">See also</span></span>



[<span data-ttu-id="5aa3f-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5aa3f-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5aa3f-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5aa3f-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5aa3f-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5aa3f-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5aa3f-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5aa3f-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

