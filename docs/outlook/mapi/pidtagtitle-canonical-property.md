---
title: PidTagTitle 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTitle
api_type:
- COM
ms.assetid: f35bbcc3-15dd-40ab-9bf4-bdb21f95d464
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 825922bec95a24fe718cdb7db82851a820c364ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803627"
---
# <a name="pidtagtitle-canonical-property"></a><span data-ttu-id="ec06c-103">PidTagTitle 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ec06c-103">PidTagTitle Canonical Property</span></span>

  
  
<span data-ttu-id="ec06c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ec06c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ec06c-105">受信者の役職が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ec06c-105">Contains the recipient's job title.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec06c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ec06c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ec06c-107">PR_TITLE、PR_TITLE_A、PR_TITLE_W</span><span class="sxs-lookup"><span data-stu-id="ec06c-107">PR_TITLE, PR_TITLE_A, PR_TITLE_W</span></span>  <br/> |
|<span data-ttu-id="ec06c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ec06c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ec06c-109">0x3A17</span><span class="sxs-lookup"><span data-stu-id="ec06c-109">0x3A17</span></span>  <br/> |
|<span data-ttu-id="ec06c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ec06c-110">Data type:</span></span>  <br/> |<span data-ttu-id="ec06c-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ec06c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ec06c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ec06c-112">Area:</span></span>  <br/> |<span data-ttu-id="ec06c-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="ec06c-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec06c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ec06c-114">Remarks</span></span>

<span data-ttu-id="ec06c-115">これらのプロパティでは、識別を提供し、受信者の情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="ec06c-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="ec06c-116">受信者と受信者の組織によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="ec06c-116">They are defined by the recipient and the recipient's organization.</span></span> 
  
<span data-ttu-id="ec06c-117">これらのプロパティは通常、受信者の正式な役職、職業はプログラマではなく、上級プログラマなどを示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec06c-117">These properties are commonly used to indicate the recipient's formal job title, such as Senior Programmer, rather than occupational class, such as programmer.</span></span> <span data-ttu-id="ec06c-118">通常 Esq. などの「接尾辞」タイトルにも使用されない</span><span class="sxs-lookup"><span data-stu-id="ec06c-118">It is not typically used for "suffix" titles such as Esq.</span></span> <span data-ttu-id="ec06c-119">または、dds を使用可能です。</span><span class="sxs-lookup"><span data-stu-id="ec06c-119">or DDS.</span></span>
  
<span data-ttu-id="ec06c-120">このプロパティの一般的な値が含まれます: マネージング ・ ディレクター、プログラマの II、同僚の教授、および開発をリードします。</span><span class="sxs-lookup"><span data-stu-id="ec06c-120">Common values for this property include: Managing Director, Programmer II, Associate Professor, and Development Lead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ec06c-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ec06c-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ec06c-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ec06c-122">Protocol specifications</span></span>

<span data-ttu-id="ec06c-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec06c-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec06c-124">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ec06c-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ec06c-125">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec06c-125">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec06c-126">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ec06c-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="ec06c-127">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec06c-127">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec06c-128">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ec06c-128">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ec06c-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ec06c-129">Header files</span></span>

<span data-ttu-id="ec06c-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ec06c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="ec06c-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ec06c-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="ec06c-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ec06c-132">Mapitags.h</span></span>
  
> <span data-ttu-id="ec06c-133">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ec06c-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec06c-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec06c-134">See also</span></span>



[<span data-ttu-id="ec06c-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ec06c-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ec06c-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ec06c-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ec06c-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ec06c-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ec06c-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ec06c-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

