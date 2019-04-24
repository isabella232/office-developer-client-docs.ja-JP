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
ms.openlocfilehash: c1d03ab8a1381609784862e7c7cf3576bc90527e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280565"
---
# <a name="pidtagkeyword-canonical-property"></a><span data-ttu-id="a2864-103">PidTagKeyword 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a2864-103">PidTagKeyword Canonical Property</span></span>

  
  
<span data-ttu-id="a2864-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2864-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2864-105">受信者のシステム管理者に対して受信者を識別するキーワードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2864-105">Contains a keyword that identifies the recipient to the recipient's system administrator.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a2864-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a2864-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a2864-107">PR_KEYWORD、PR_KEYWORD_A、PR_KEYWORD_W</span><span class="sxs-lookup"><span data-stu-id="a2864-107">PR_KEYWORD, PR_KEYWORD_A, PR_KEYWORD_W</span></span>  <br/> |
|<span data-ttu-id="a2864-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a2864-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a2864-109">0x3A0B</span><span class="sxs-lookup"><span data-stu-id="a2864-109">0x3A0B</span></span>  <br/> |
|<span data-ttu-id="a2864-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a2864-110">Data type:</span></span>  <br/> |<span data-ttu-id="a2864-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a2864-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a2864-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a2864-112">Area:</span></span>  <br/> |<span data-ttu-id="a2864-113">Address</span><span class="sxs-lookup"><span data-stu-id="a2864-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2864-114">解説</span><span class="sxs-lookup"><span data-stu-id="a2864-114">Remarks</span></span>

<span data-ttu-id="a2864-115">これらのプロパティは、受信者の id とアクセス情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a2864-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="a2864-116">受信者と組織で定義されています。</span><span class="sxs-lookup"><span data-stu-id="a2864-116">They are defined by the recipient and their organization.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a2864-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a2864-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a2864-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a2864-118">Protocol specifications</span></span>

<span data-ttu-id="a2864-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2864-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2864-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a2864-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a2864-121">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2864-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2864-122">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a2864-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a2864-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a2864-123">Header files</span></span>

<span data-ttu-id="a2864-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a2864-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="a2864-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a2864-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="a2864-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="a2864-126">Mapitags.h</span></span>
  
> <span data-ttu-id="a2864-127">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a2864-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2864-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="a2864-128">See also</span></span>



[<span data-ttu-id="a2864-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a2864-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a2864-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a2864-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a2864-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a2864-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a2864-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a2864-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

