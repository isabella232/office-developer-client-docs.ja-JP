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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338697"
---
# <a name="pidtagpostaladdress-canonical-property"></a><span data-ttu-id="dcf75-103">PidTagPostalAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dcf75-103">PidTagPostalAddress Canonical Property</span></span>

  
  
<span data-ttu-id="dcf75-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcf75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcf75-105">受信者の住所を含みます。</span><span class="sxs-lookup"><span data-stu-id="dcf75-105">Contains the recipient's postal address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dcf75-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="dcf75-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dcf75-107">PR_POSTAL_ADDRESS、PR_POSTAL_ADDRESS_A、PR_POSTAL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="dcf75-107">PR_POSTAL_ADDRESS, PR_POSTAL_ADDRESS_A, PR_POSTAL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="dcf75-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="dcf75-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dcf75-109">0x3a15</span><span class="sxs-lookup"><span data-stu-id="dcf75-109">0x3A15</span></span>  <br/> |
|<span data-ttu-id="dcf75-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="dcf75-110">Data type:</span></span>  <br/> |<span data-ttu-id="dcf75-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dcf75-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dcf75-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="dcf75-112">Area:</span></span>  <br/> |<span data-ttu-id="dcf75-113">MAPI メールユーザー</span><span class="sxs-lookup"><span data-stu-id="dcf75-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dcf75-114">解説</span><span class="sxs-lookup"><span data-stu-id="dcf75-114">Remarks</span></span>

<span data-ttu-id="dcf75-115">これらのプロパティは、受信者の id とアクセス情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="dcf75-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="dcf75-116">受信者と受信者の組織によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="dcf75-116">They are defined by the recipient and the recipient's organization.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dcf75-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="dcf75-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dcf75-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="dcf75-118">Protocol specifications</span></span>

<span data-ttu-id="dcf75-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcf75-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcf75-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="dcf75-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dcf75-121">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcf75-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcf75-122">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="dcf75-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dcf75-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="dcf75-123">Header files</span></span>

<span data-ttu-id="dcf75-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dcf75-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="dcf75-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="dcf75-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="dcf75-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="dcf75-126">Mapitags.h</span></span>
  
> <span data-ttu-id="dcf75-127">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dcf75-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dcf75-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="dcf75-128">See also</span></span>



[<span data-ttu-id="dcf75-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="dcf75-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dcf75-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dcf75-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dcf75-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="dcf75-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dcf75-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="dcf75-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

