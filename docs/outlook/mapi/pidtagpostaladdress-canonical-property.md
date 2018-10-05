---
title: PidTagPostalAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPostalAddress
api_type:
- COM
ms.assetid: cf400713-3b42-4ee7-9dea-d52b8bf03ac3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f6f67572914ae7dbcc6e6d6b992fb2f8ee463117
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383311"
---
# <a name="pidtagpostaladdress-canonical-property"></a><span data-ttu-id="e5178-103">PidTagPostalAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e5178-103">PidTagPostalAddress Canonical Property</span></span>

  
  
<span data-ttu-id="e5178-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5178-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5178-105">受信者の郵便番号と住所が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e5178-105">Contains the recipient's postal address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5178-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e5178-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e5178-107">PR_POSTAL_ADDRESS、PR_POSTAL_ADDRESS_A、PR_POSTAL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="e5178-107">PR_POSTAL_ADDRESS, PR_POSTAL_ADDRESS_A, PR_POSTAL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="e5178-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e5178-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e5178-109">0x3A15</span><span class="sxs-lookup"><span data-stu-id="e5178-109">0x3A15</span></span>  <br/> |
|<span data-ttu-id="e5178-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e5178-110">Data type:</span></span>  <br/> |<span data-ttu-id="e5178-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e5178-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e5178-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e5178-112">Area:</span></span>  <br/> |<span data-ttu-id="e5178-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="e5178-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5178-114">備考</span><span class="sxs-lookup"><span data-stu-id="e5178-114">Remarks</span></span>

<span data-ttu-id="e5178-115">これらのプロパティでは、識別を提供し、受信者の情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="e5178-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="e5178-116">受信者と受信者の組織によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="e5178-116">They are defined by the recipient and the recipient's organization.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e5178-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e5178-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e5178-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e5178-118">Protocol specifications</span></span>

<span data-ttu-id="e5178-119">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5178-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5178-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e5178-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e5178-121">[[MS OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5178-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5178-122">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5178-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e5178-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e5178-123">Header files</span></span>

<span data-ttu-id="e5178-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5178-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="e5178-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e5178-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="e5178-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e5178-126">Mapitags.h</span></span>
  
> <span data-ttu-id="e5178-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e5178-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5178-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5178-128">See also</span></span>



[<span data-ttu-id="e5178-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e5178-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e5178-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e5178-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e5178-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e5178-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e5178-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e5178-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

