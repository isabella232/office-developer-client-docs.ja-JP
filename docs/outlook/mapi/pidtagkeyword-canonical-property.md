---
title: PidTagKeyword 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagKeyword
api_type:
- HeaderDef
ms.assetid: 8dbfb22d-93db-468c-b2a4-eaa2b545bd61
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 40c61c2c34fa81c1b025c740b73bfe2d8b1f0969
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802938"
---
# <a name="pidtagkeyword-canonical-property"></a><span data-ttu-id="fb141-103">PidTagKeyword 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fb141-103">PidTagKeyword Canonical Property</span></span>

  
  
<span data-ttu-id="fb141-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb141-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb141-105">受信者は受信者のシステム管理者を指定するキーワードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fb141-105">Contains a keyword that identifies the recipient to the recipient's system administrator.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fb141-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fb141-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fb141-107">PR_KEYWORD、PR_KEYWORD_A、PR_KEYWORD_W</span><span class="sxs-lookup"><span data-stu-id="fb141-107">PR_KEYWORD, PR_KEYWORD_A, PR_KEYWORD_W</span></span>  <br/> |
|<span data-ttu-id="fb141-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fb141-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fb141-109">0x3A0B</span><span class="sxs-lookup"><span data-stu-id="fb141-109">0x3A0B</span></span>  <br/> |
|<span data-ttu-id="fb141-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fb141-110">Data type:</span></span>  <br/> |<span data-ttu-id="fb141-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="fb141-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="fb141-112">領域:</span><span class="sxs-lookup"><span data-stu-id="fb141-112">Area:</span></span>  <br/> |<span data-ttu-id="fb141-113">Address</span><span class="sxs-lookup"><span data-stu-id="fb141-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb141-114">注釈</span><span class="sxs-lookup"><span data-stu-id="fb141-114">Remarks</span></span>

<span data-ttu-id="fb141-115">これらのプロパティでは、識別を提供し、受信者の情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="fb141-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="fb141-116">受信者とその構造によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="fb141-116">They are defined by the recipient and their organization.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fb141-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fb141-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fb141-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fb141-118">Protocol specifications</span></span>

<span data-ttu-id="fb141-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb141-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb141-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fb141-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fb141-121">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb141-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb141-122">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="fb141-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fb141-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fb141-123">Header files</span></span>

<span data-ttu-id="fb141-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb141-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="fb141-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fb141-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="fb141-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fb141-126">Mapitags.h</span></span>
  
> <span data-ttu-id="fb141-127">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fb141-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb141-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="fb141-128">See also</span></span>



[<span data-ttu-id="fb141-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fb141-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fb141-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fb141-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fb141-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fb141-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fb141-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fb141-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

