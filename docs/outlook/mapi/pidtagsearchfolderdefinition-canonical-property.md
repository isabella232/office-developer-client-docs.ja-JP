---
title: PidTagSearchFolderDefinition 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderDefinition
api_type:
- COM
ms.assetid: a61056e7-365c-4972-abf7-26e2ab07105d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3b4e5fa7228cf243c79a8ec0c9e2b73b7da21c6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336359"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a><span data-ttu-id="9035c-103">PidTagSearchFolderDefinition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9035c-103">PidTagSearchFolderDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="9035c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9035c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9035c-105">検索条件を指定するデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="9035c-105">Contains data that specifies the search criteria.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9035c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9035c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9035c-107">PR_WB_SF_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="9035c-107">PR_WB_SF_DEFINITION</span></span>  <br/> |
|<span data-ttu-id="9035c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9035c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9035c-109">0x684 5</span><span class="sxs-lookup"><span data-stu-id="9035c-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="9035c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9035c-110">Data type:</span></span>  <br/> |<span data-ttu-id="9035c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9035c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9035c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9035c-112">Area:</span></span>  <br/> |<span data-ttu-id="9035c-113">検索</span><span class="sxs-lookup"><span data-stu-id="9035c-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9035c-114">解説</span><span class="sxs-lookup"><span data-stu-id="9035c-114">Remarks</span></span>

<span data-ttu-id="9035c-115">このプロパティに含まれるバイナリラージオブジェクト (BLOB) の各フィールドの特定のコンテンツは、 **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)) プロパティで指定されているテンプレート ID によって異なります。</span><span class="sxs-lookup"><span data-stu-id="9035c-115">The specific content of each field of the binary large object (BLOB) contained in this property is dependent upon the template ID that is specified in **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="9035c-116">BLOB 構造および検索テンプレートの詳細については、「 [[OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9035c-116">For information about the BLOB structure and search templates, see [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9035c-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9035c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9035c-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9035c-118">Protocol specifications</span></span>

<span data-ttu-id="9035c-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9035c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9035c-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9035c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9035c-121">[[OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9035c-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9035c-122">検索フォルダーリストの構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9035c-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9035c-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9035c-123">Header files</span></span>

<span data-ttu-id="9035c-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9035c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9035c-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9035c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9035c-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="9035c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9035c-127">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9035c-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9035c-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9035c-128">See also</span></span>



[<span data-ttu-id="9035c-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9035c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9035c-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9035c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9035c-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9035c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9035c-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9035c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

