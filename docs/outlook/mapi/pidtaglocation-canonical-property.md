---
title: PidTagLocation 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLocation
api_type:
- HeaderDef
ms.assetid: 99dffcd9-83dc-462e-b0ce-e2101e546cc6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 558db0d89103d02f37297c058384cac96ea9ca26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278786"
---
# <a name="pidtaglocation-canonical-property"></a><span data-ttu-id="377cd-103">PidTagLocation 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="377cd-103">PidTagLocation Canonical Property</span></span>

  
  
<span data-ttu-id="377cd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="377cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="377cd-105">受信者の組織にとって便利な形式の受信者の場所が含まれています。</span><span class="sxs-lookup"><span data-stu-id="377cd-105">Contains the location of the recipient in a format that is useful to the recipient's organization.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="377cd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="377cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="377cd-107">PR_LOCATION、PR_LOCATION_A、PR_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="377cd-107">PR_LOCATION, PR_LOCATION_A, PR_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="377cd-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="377cd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="377cd-109">0x3A0D</span><span class="sxs-lookup"><span data-stu-id="377cd-109">0x3A0D</span></span>  <br/> |
|<span data-ttu-id="377cd-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="377cd-110">Data type:</span></span>  <br/> |<span data-ttu-id="377cd-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="377cd-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="377cd-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="377cd-112">Area:</span></span>  <br/> |<span data-ttu-id="377cd-113">Address</span><span class="sxs-lookup"><span data-stu-id="377cd-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="377cd-114">解説</span><span class="sxs-lookup"><span data-stu-id="377cd-114">Remarks</span></span>

<span data-ttu-id="377cd-115">これらのプロパティは、受信者の id とアクセス情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="377cd-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="377cd-116">受信者と組織で定義されています。</span><span class="sxs-lookup"><span data-stu-id="377cd-116">They are defined by the recipient and their organization.</span></span> 
  
<span data-ttu-id="377cd-117">コンテンツは、受信者の組織のニーズによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="377cd-117">The contents are defined by the needs of the recipient's organization.</span></span> <span data-ttu-id="377cd-118">たとえば、組織によっては、建物番号とオフィス番号を指定してメッセージングユーザーを特定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="377cd-118">For example, some organizations might identify messaging users by specifying the building number and office number.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="377cd-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="377cd-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="377cd-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="377cd-120">Protocol specifications</span></span>

<span data-ttu-id="377cd-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="377cd-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="377cd-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="377cd-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="377cd-123">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="377cd-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="377cd-124">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="377cd-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="377cd-125">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="377cd-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="377cd-126">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="377cd-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="377cd-127">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="377cd-127">Header files</span></span>

<span data-ttu-id="377cd-128">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="377cd-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="377cd-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="377cd-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="377cd-130">Mapitags</span><span class="sxs-lookup"><span data-stu-id="377cd-130">Mapitags.h</span></span>
  
> <span data-ttu-id="377cd-131">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="377cd-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="377cd-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="377cd-132">See also</span></span>



[<span data-ttu-id="377cd-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="377cd-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="377cd-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="377cd-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="377cd-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="377cd-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="377cd-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="377cd-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

