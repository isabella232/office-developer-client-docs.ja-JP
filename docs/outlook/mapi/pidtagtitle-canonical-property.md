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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2501ea7c4be08b0bec3c2d65e6a504df47dfc488
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358766"
---
# <a name="pidtagtitle-canonical-property"></a><span data-ttu-id="a01bb-103">PidTagTitle 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a01bb-103">PidTagTitle Canonical Property</span></span>

  
  
<span data-ttu-id="a01bb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a01bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a01bb-105">受信者の役職が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a01bb-105">Contains the recipient's job title.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a01bb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a01bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a01bb-107">PR_TITLE、PR_TITLE_A、PR_TITLE_W</span><span class="sxs-lookup"><span data-stu-id="a01bb-107">PR_TITLE, PR_TITLE_A, PR_TITLE_W</span></span>  <br/> |
|<span data-ttu-id="a01bb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a01bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a01bb-109">0x3A17</span><span class="sxs-lookup"><span data-stu-id="a01bb-109">0x3A17</span></span>  <br/> |
|<span data-ttu-id="a01bb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a01bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="a01bb-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a01bb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a01bb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a01bb-112">Area:</span></span>  <br/> |<span data-ttu-id="a01bb-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="a01bb-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a01bb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a01bb-114">Remarks</span></span>

<span data-ttu-id="a01bb-115">これらのプロパティは、受信者の ID とアクセス情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a01bb-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="a01bb-116">受信者と受信者の組織によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="a01bb-116">They are defined by the recipient and the recipient's organization.</span></span> 
  
<span data-ttu-id="a01bb-117">これらのプロパティは、通常、プログラマなどの職業クラスではなく、シニア プログラマなどの受信者の正式な役職を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a01bb-117">These properties are commonly used to indicate the recipient's formal job title, such as Senior Programmer, rather than occupational class, such as programmer.</span></span> <span data-ttu-id="a01bb-118">通常、Esq などの "サフィックス" タイトルには使用されません。</span><span class="sxs-lookup"><span data-stu-id="a01bb-118">It is not typically used for "suffix" titles such as Esq.</span></span> <span data-ttu-id="a01bb-119">または DDS。</span><span class="sxs-lookup"><span data-stu-id="a01bb-119">or DDS.</span></span>
  
<span data-ttu-id="a01bb-120">このプロパティの一般的な値は、マネージング ディレクター、プログラマ II、准教授、開発リードです。</span><span class="sxs-lookup"><span data-stu-id="a01bb-120">Common values for this property include: Managing Director, Programmer II, Associate Professor, and Development Lead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a01bb-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a01bb-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a01bb-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a01bb-122">Protocol specifications</span></span>

<span data-ttu-id="a01bb-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a01bb-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a01bb-124">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="a01bb-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a01bb-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a01bb-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a01bb-126">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a01bb-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="a01bb-127">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a01bb-127">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a01bb-128">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a01bb-128">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a01bb-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a01bb-129">Header files</span></span>

<span data-ttu-id="a01bb-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a01bb-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="a01bb-131">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a01bb-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="a01bb-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a01bb-132">Mapitags.h</span></span>
  
> <span data-ttu-id="a01bb-133">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a01bb-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a01bb-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="a01bb-134">See also</span></span>



[<span data-ttu-id="a01bb-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a01bb-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a01bb-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a01bb-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a01bb-137">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a01bb-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a01bb-138">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a01bb-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

