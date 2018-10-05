---
title: PidTagGender 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGender
api_type:
- HeaderDef
ms.assetid: a79a139a-6813-49f6-b622-bb66d62c4462
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b8ce3898ac021bc6eec2af6220889d71ff5a18dc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386615"
---
# <a name="pidtaggender-canonical-property"></a><span data-ttu-id="95e3c-103">PidTagGender 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="95e3c-103">PidTagGender Canonical Property</span></span>

  
  
<span data-ttu-id="95e3c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95e3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95e3c-105">メッセージング ユーザーの性別が含まれています。</span><span class="sxs-lookup"><span data-stu-id="95e3c-105">Contains the gender of the messaging user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95e3c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="95e3c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95e3c-107">PR_GENDER</span><span class="sxs-lookup"><span data-stu-id="95e3c-107">PR_GENDER</span></span>  <br/> |
|<span data-ttu-id="95e3c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="95e3c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="95e3c-109">0x3A4D</span><span class="sxs-lookup"><span data-stu-id="95e3c-109">0x3A4D</span></span>  <br/> |
|<span data-ttu-id="95e3c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="95e3c-110">Data type:</span></span>  <br/> |<span data-ttu-id="95e3c-111">PT_I2</span><span class="sxs-lookup"><span data-stu-id="95e3c-111">PT_I2</span></span>  <br/> |
|<span data-ttu-id="95e3c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="95e3c-112">Area:</span></span>  <br/> |<span data-ttu-id="95e3c-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="95e3c-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95e3c-114">備考</span><span class="sxs-lookup"><span data-stu-id="95e3c-114">Remarks</span></span>

<span data-ttu-id="95e3c-115">このプロパティは、id およびメッセージングのユーザーに関する情報にアクセスを提供し、コンテンツは。</span><span class="sxs-lookup"><span data-stu-id="95e3c-115">This property provides identification and access information about a messaging user and the content is.</span></span> <span data-ttu-id="95e3c-116">コンテンツは、メッセージングのユーザーとメッセージのユーザーの組織によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="95e3c-116">The content is defined by the messaging user and the messaging user's organization.</span></span> 
  
<span data-ttu-id="95e3c-117">このプロパティの有効な値は、性別の列挙体で定義されます。</span><span class="sxs-lookup"><span data-stu-id="95e3c-117">The possible values for this property are defined in the gender enumeration.</span></span> <span data-ttu-id="95e3c-118">これらは以下のとおり。</span><span class="sxs-lookup"><span data-stu-id="95e3c-118">They are listed as follows:</span></span>
  
|<span data-ttu-id="95e3c-119">**性別の列挙**</span><span class="sxs-lookup"><span data-stu-id="95e3c-119">**Gender enumeration**</span></span>|<span data-ttu-id="95e3c-120">**値**</span><span class="sxs-lookup"><span data-stu-id="95e3c-120">**Value**</span></span>|<span data-ttu-id="95e3c-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="95e3c-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="95e3c-122">genderUnspecified</span><span class="sxs-lookup"><span data-stu-id="95e3c-122">genderUnspecified</span></span>  <br/> |<span data-ttu-id="95e3c-123">0x0000</span><span class="sxs-lookup"><span data-stu-id="95e3c-123">0x0000</span></span>  <br/> |<span data-ttu-id="95e3c-124">連絡先の性別が指定されていません。</span><span class="sxs-lookup"><span data-stu-id="95e3c-124">The contact's gender is unspecified.</span></span>  <br/> |
|<span data-ttu-id="95e3c-125">genderFemale</span><span class="sxs-lookup"><span data-stu-id="95e3c-125">genderFemale</span></span>  <br/> |<span data-ttu-id="95e3c-126">0x0001</span><span class="sxs-lookup"><span data-stu-id="95e3c-126">0x0001</span></span>  <br/> |<span data-ttu-id="95e3c-127">連絡先は、(メス) です。</span><span class="sxs-lookup"><span data-stu-id="95e3c-127">The contact is female.</span></span>  <br/> |
|<span data-ttu-id="95e3c-128">genderMale</span><span class="sxs-lookup"><span data-stu-id="95e3c-128">genderMale</span></span>  <br/> |<span data-ttu-id="95e3c-129">0x0002</span><span class="sxs-lookup"><span data-stu-id="95e3c-129">0x0002</span></span>  <br/> |<span data-ttu-id="95e3c-130">連絡先は、(オス) です。</span><span class="sxs-lookup"><span data-stu-id="95e3c-130">The contact is male.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="95e3c-131">関連リソース</span><span class="sxs-lookup"><span data-stu-id="95e3c-131">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="95e3c-132">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="95e3c-132">Protocol specifications</span></span>

<span data-ttu-id="95e3c-133">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95e3c-133">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95e3c-134">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="95e3c-134">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="95e3c-135">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95e3c-135">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95e3c-136">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="95e3c-136">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="95e3c-137">[[MS OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95e3c-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95e3c-138">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="95e3c-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="95e3c-139">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="95e3c-139">Header files</span></span>

<span data-ttu-id="95e3c-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95e3c-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="95e3c-141">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="95e3c-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="95e3c-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="95e3c-142">Mapitags.h</span></span>
  
> <span data-ttu-id="95e3c-143">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="95e3c-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95e3c-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="95e3c-144">See also</span></span>



[<span data-ttu-id="95e3c-145">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="95e3c-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95e3c-146">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="95e3c-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95e3c-147">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="95e3c-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95e3c-148">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="95e3c-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

