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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 67be9232d7e80dbbabe93fbe408b3d3fc8b832ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338522"
---
# <a name="pidtagpostalcode-canonical-property"></a><span data-ttu-id="00c78-103">PidTagPostalCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="00c78-103">PidTagPostalCode Canonical Property</span></span>

  
  
<span data-ttu-id="00c78-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00c78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00c78-105">受信者の郵便番号を格納します。</span><span class="sxs-lookup"><span data-stu-id="00c78-105">Contains the postal code for the recipient's postal address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00c78-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="00c78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00c78-107">PR_POSTAL_CODE、PR_POSTAL_CODE_A、PR_POSTAL_CODE_W、PR_BUSINESS_ADDRESS_POSTAL_CODE、PR_BUSINESS_ADDRESS_POSTAL_CODE_A、PR_BUSINESS_ADDRESS_POSTAL_CODE_W</span><span class="sxs-lookup"><span data-stu-id="00c78-107">PR_POSTAL_CODE, PR_POSTAL_CODE_A, PR_POSTAL_CODE_W, PR_BUSINESS_ADDRESS_POSTAL_CODE, PR_BUSINESS_ADDRESS_POSTAL_CODE_A, PR_BUSINESS_ADDRESS_POSTAL_CODE_W</span></span>  <br/> |
|<span data-ttu-id="00c78-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="00c78-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00c78-109">0x3A2A</span><span class="sxs-lookup"><span data-stu-id="00c78-109">0x3A2A</span></span>  <br/> |
|<span data-ttu-id="00c78-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="00c78-110">Data type:</span></span>  <br/> |<span data-ttu-id="00c78-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="00c78-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="00c78-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="00c78-112">Area:</span></span>  <br/> |<span data-ttu-id="00c78-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="00c78-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00c78-114">注釈</span><span class="sxs-lookup"><span data-stu-id="00c78-114">Remarks</span></span>

<span data-ttu-id="00c78-115">これらのプロパティは、受信者の ID とアクセス情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="00c78-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="00c78-116">受信者とその組織によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="00c78-116">They are defined by the recipient and their organization.</span></span> 
  
<span data-ttu-id="00c78-117">郵便番号は、受信者の国/地域に固有です。</span><span class="sxs-lookup"><span data-stu-id="00c78-117">The postal code is specific to the recipient's country/region.</span></span> <span data-ttu-id="00c78-118">米国では、このプロパティには ZIP コードが含まれる。</span><span class="sxs-lookup"><span data-stu-id="00c78-118">In the United States of America, this property contains the ZIP code.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="00c78-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="00c78-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00c78-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="00c78-120">Protocol specifications</span></span>

<span data-ttu-id="00c78-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00c78-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00c78-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="00c78-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00c78-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00c78-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00c78-124">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="00c78-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="00c78-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00c78-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00c78-126">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="00c78-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00c78-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="00c78-127">Header files</span></span>

<span data-ttu-id="00c78-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00c78-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="00c78-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="00c78-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="00c78-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="00c78-130">Mapitags.h</span></span>
  
> <span data-ttu-id="00c78-131">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="00c78-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00c78-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="00c78-132">See also</span></span>



[<span data-ttu-id="00c78-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="00c78-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00c78-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="00c78-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00c78-135">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="00c78-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00c78-136">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="00c78-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

