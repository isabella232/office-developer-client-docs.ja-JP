---
title: PidTagSearchFolderTemplateId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderTemplateId
api_type:
- COM
ms.assetid: 56288f55-b3ba-42df-9c90-f9b5857f19a1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bee22a7a435b99f4b94473a3f6eb4b7f32517128
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336625"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a><span data-ttu-id="a0422-103">PidTagSearchFolderTemplateId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0422-103">PidTagSearchFolderTemplateId Canonical Property</span></span>

  
  
<span data-ttu-id="a0422-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0422-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0422-105">検索に使用されているテンプレートの ID を格納します。</span><span class="sxs-lookup"><span data-stu-id="a0422-105">Contains the ID of the template that is being used for the search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0422-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a0422-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0422-107">PR_WB_SF_TEMPLATE_ID</span><span class="sxs-lookup"><span data-stu-id="a0422-107">PR_WB_SF_TEMPLATE_ID</span></span>  <br/> |
|<span data-ttu-id="a0422-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a0422-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a0422-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="a0422-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="a0422-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a0422-110">Data type:</span></span>  <br/> |<span data-ttu-id="a0422-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a0422-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a0422-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a0422-112">Area:</span></span>  <br/> |<span data-ttu-id="a0422-113">検索</span><span class="sxs-lookup"><span data-stu-id="a0422-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0422-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a0422-114">Remarks</span></span>

<span data-ttu-id="a0422-115">検索フォルダーの条件は、テンプレートによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="a0422-115">Search folder criteria is specified by a template.</span></span> <span data-ttu-id="a0422-116">検索フォルダーを定義するメッセージのこのプロパティは、対応するテンプレートを識別します。</span><span class="sxs-lookup"><span data-stu-id="a0422-116">This property on the message that defines the search folder identifies its corresponding template.</span></span> <span data-ttu-id="a0422-117">テンプレートは、検索条件の定義に加えて、検索から除外するフォルダーを定義し、検索から除外するアイテムを定義し **、PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType)](pidtagsearchfolderstoragetype-canonical-property.md)の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0422-117">In addition to defining search criteria, a template also defines folders to exclude from the search, defines items to exclude from the search, and specifies the value of **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span></span>
  
<span data-ttu-id="a0422-118">検索フォルダー テンプレートの詳細については [、「[MS-OXOSRCH] 」を参照してください](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="a0422-118">For more information about Search Folder Templates see [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a0422-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a0422-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a0422-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a0422-120">Protocol specifications</span></span>

<span data-ttu-id="a0422-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0422-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0422-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="a0422-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a0422-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0422-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0422-124">検索フォルダー 一覧の構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0422-124">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a0422-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a0422-125">Header files</span></span>

<span data-ttu-id="a0422-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0422-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0422-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a0422-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a0422-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a0422-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a0422-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a0422-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0422-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0422-130">See also</span></span>



[<span data-ttu-id="a0422-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a0422-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0422-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0422-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0422-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a0422-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0422-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a0422-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

