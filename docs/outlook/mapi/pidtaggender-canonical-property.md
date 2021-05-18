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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b8ce3898ac021bc6eec2af6220889d71ff5a18dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316157"
---
# <a name="pidtaggender-canonical-property"></a><span data-ttu-id="19a8a-103">PidTagGender 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="19a8a-103">PidTagGender Canonical Property</span></span>

  
  
<span data-ttu-id="19a8a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19a8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19a8a-105">メッセージング ユーザーの性別が含まれる。</span><span class="sxs-lookup"><span data-stu-id="19a8a-105">Contains the gender of the messaging user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19a8a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="19a8a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19a8a-107">PR_GENDER</span><span class="sxs-lookup"><span data-stu-id="19a8a-107">PR_GENDER</span></span>  <br/> |
|<span data-ttu-id="19a8a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="19a8a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="19a8a-109">0x3A4D</span><span class="sxs-lookup"><span data-stu-id="19a8a-109">0x3A4D</span></span>  <br/> |
|<span data-ttu-id="19a8a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="19a8a-110">Data type:</span></span>  <br/> |<span data-ttu-id="19a8a-111">PT_I2</span><span class="sxs-lookup"><span data-stu-id="19a8a-111">PT_I2</span></span>  <br/> |
|<span data-ttu-id="19a8a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="19a8a-112">Area:</span></span>  <br/> |<span data-ttu-id="19a8a-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="19a8a-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19a8a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="19a8a-114">Remarks</span></span>

<span data-ttu-id="19a8a-115">このプロパティは、メッセージング ユーザーとコンテンツに関する識別情報とアクセス情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="19a8a-115">This property provides identification and access information about a messaging user and the content is.</span></span> <span data-ttu-id="19a8a-116">コンテンツは、メッセージング ユーザーとメッセージング ユーザーの組織によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="19a8a-116">The content is defined by the messaging user and the messaging user's organization.</span></span> 
  
<span data-ttu-id="19a8a-117">このプロパティに使用できる値は、性別列挙で定義されます。</span><span class="sxs-lookup"><span data-stu-id="19a8a-117">The possible values for this property are defined in the gender enumeration.</span></span> <span data-ttu-id="19a8a-118">これらは、次のように一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="19a8a-118">They are listed as follows:</span></span>
  
|<span data-ttu-id="19a8a-119">**性別列挙**</span><span class="sxs-lookup"><span data-stu-id="19a8a-119">**Gender enumeration**</span></span>|<span data-ttu-id="19a8a-120">**値**</span><span class="sxs-lookup"><span data-stu-id="19a8a-120">**Value**</span></span>|<span data-ttu-id="19a8a-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="19a8a-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="19a8a-122">genderUnspecified</span><span class="sxs-lookup"><span data-stu-id="19a8a-122">genderUnspecified</span></span>  <br/> |<span data-ttu-id="19a8a-123">0x0000</span><span class="sxs-lookup"><span data-stu-id="19a8a-123">0x0000</span></span>  <br/> |<span data-ttu-id="19a8a-124">連絡先の性別は指定されていません。</span><span class="sxs-lookup"><span data-stu-id="19a8a-124">The contact's gender is unspecified.</span></span>  <br/> |
|<span data-ttu-id="19a8a-125">genderFemale</span><span class="sxs-lookup"><span data-stu-id="19a8a-125">genderFemale</span></span>  <br/> |<span data-ttu-id="19a8a-126">0x0001</span><span class="sxs-lookup"><span data-stu-id="19a8a-126">0x0001</span></span>  <br/> |<span data-ttu-id="19a8a-127">連絡先は女性です。</span><span class="sxs-lookup"><span data-stu-id="19a8a-127">The contact is female.</span></span>  <br/> |
|<span data-ttu-id="19a8a-128">genderMale</span><span class="sxs-lookup"><span data-stu-id="19a8a-128">genderMale</span></span>  <br/> |<span data-ttu-id="19a8a-129">0x0002</span><span class="sxs-lookup"><span data-stu-id="19a8a-129">0x0002</span></span>  <br/> |<span data-ttu-id="19a8a-130">連絡先は男性です。</span><span class="sxs-lookup"><span data-stu-id="19a8a-130">The contact is male.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="19a8a-131">関連リソース</span><span class="sxs-lookup"><span data-stu-id="19a8a-131">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="19a8a-132">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="19a8a-132">Protocol specifications</span></span>

<span data-ttu-id="19a8a-133">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19a8a-133">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19a8a-134">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="19a8a-134">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="19a8a-135">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19a8a-135">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19a8a-136">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="19a8a-136">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="19a8a-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19a8a-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19a8a-138">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="19a8a-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="19a8a-139">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="19a8a-139">Header files</span></span>

<span data-ttu-id="19a8a-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19a8a-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="19a8a-141">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="19a8a-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="19a8a-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="19a8a-142">Mapitags.h</span></span>
  
> <span data-ttu-id="19a8a-143">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="19a8a-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19a8a-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="19a8a-144">See also</span></span>



[<span data-ttu-id="19a8a-145">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="19a8a-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19a8a-146">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="19a8a-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19a8a-147">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="19a8a-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19a8a-148">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="19a8a-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

