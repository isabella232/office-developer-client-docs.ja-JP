---
title: PidTagGovernmentIdNumber 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGovernmentIdNumber
api_type:
- HeaderDef
ms.assetid: fa265d37-a1ea-4812-8fe9-21dac374cd7c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4b7ce4620f224597e753fb05ec377461b4c19c9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316150"
---
# <a name="pidtaggovernmentidnumber-canonical-property"></a><span data-ttu-id="afc00-103">PidTagGovernmentIdNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="afc00-103">PidTagGovernmentIdNumber Canonical Property</span></span>

  
  
<span data-ttu-id="afc00-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="afc00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="afc00-105">受信者の自治体識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="afc00-105">Contains a government identifier for the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="afc00-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="afc00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="afc00-107">PR_GOVERNMENT_ID_NUMBER、PR_GOVERNMENT_ID_NUMBER_A、PR_GOVERNMENT_ID_NUMBER_W</span><span class="sxs-lookup"><span data-stu-id="afc00-107">PR_GOVERNMENT_ID_NUMBER, PR_GOVERNMENT_ID_NUMBER_A, PR_GOVERNMENT_ID_NUMBER_W</span></span>  <br/> |
|<span data-ttu-id="afc00-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="afc00-108">Identifier:</span></span>  <br/> |<span data-ttu-id="afc00-109">0x3A07</span><span class="sxs-lookup"><span data-stu-id="afc00-109">0x3A07</span></span>  <br/> |
|<span data-ttu-id="afc00-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="afc00-110">Data type:</span></span>  <br/> |<span data-ttu-id="afc00-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="afc00-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="afc00-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="afc00-112">Area:</span></span>  <br/> |<span data-ttu-id="afc00-113">MAPI メールユーザー</span><span class="sxs-lookup"><span data-stu-id="afc00-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="afc00-114">解説</span><span class="sxs-lookup"><span data-stu-id="afc00-114">Remarks</span></span>

<span data-ttu-id="afc00-115">これらのプロパティは、受信者に関する id とアクセス情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="afc00-115">These properties provide identification and access information about a recipient.</span></span> <span data-ttu-id="afc00-116">受信者と受信者の組織によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="afc00-116">They are defined by the recipient and the recipient's organization.</span></span> 
  
<span data-ttu-id="afc00-117">これらのプロパティは、通常、パスポート番号、市民番号、または社会保障番号などの納税者番号に設定されます。</span><span class="sxs-lookup"><span data-stu-id="afc00-117">These properties are commonly set to a passport number, citizen number, or taxpayer number such as a Social Security number.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="afc00-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="afc00-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="afc00-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="afc00-119">Protocol specifications</span></span>

<span data-ttu-id="afc00-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="afc00-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="afc00-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="afc00-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="afc00-122">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="afc00-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="afc00-123">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="afc00-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="afc00-124">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="afc00-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="afc00-125">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="afc00-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="afc00-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="afc00-126">Header files</span></span>

<span data-ttu-id="afc00-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="afc00-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="afc00-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="afc00-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="afc00-129">Mapitags</span><span class="sxs-lookup"><span data-stu-id="afc00-129">Mapitags.h</span></span>
  
> <span data-ttu-id="afc00-130">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="afc00-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="afc00-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="afc00-131">See also</span></span>



[<span data-ttu-id="afc00-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="afc00-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="afc00-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="afc00-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="afc00-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="afc00-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="afc00-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="afc00-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

