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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4e752d3264a64ad7b467947c44d01eb7c47ec863
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803503"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a><span data-ttu-id="c3216-103">PidTagSearchFolderTemplateId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c3216-103">PidTagSearchFolderTemplateId Canonical Property</span></span>

  
  
<span data-ttu-id="c3216-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c3216-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c3216-105">検索に使用されているテンプレートの ID が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c3216-105">Contains the ID of the template that is being used for the search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c3216-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c3216-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c3216-107">PR_WB_SF_TEMPLATE_ID</span><span class="sxs-lookup"><span data-stu-id="c3216-107">PR_WB_SF_TEMPLATE_ID</span></span>  <br/> |
|<span data-ttu-id="c3216-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c3216-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c3216-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="c3216-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="c3216-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c3216-110">Data type:</span></span>  <br/> |<span data-ttu-id="c3216-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c3216-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c3216-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c3216-112">Area:</span></span>  <br/> |<span data-ttu-id="c3216-113">検索</span><span class="sxs-lookup"><span data-stu-id="c3216-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3216-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c3216-114">Remarks</span></span>

<span data-ttu-id="c3216-115">検索フォルダーの条件は、テンプレートによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="c3216-115">Search folder criteria is specified by a template.</span></span> <span data-ttu-id="c3216-116">検索フォルダーを定義するメッセージには、このプロパティは、対応するテンプレートを識別します。</span><span class="sxs-lookup"><span data-stu-id="c3216-116">This property on the message that defines the search folder identifies its corresponding template.</span></span> <span data-ttu-id="c3216-117">検索条件を定義するには、テンプレートも検索から除外するフォルダーを定義、検索から除外する項目を定義および**PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c3216-117">In addition to defining search criteria, a template also defines folders to exclude from the search, defines items to exclude from the search, and specifies the value of **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span></span>
  
<span data-ttu-id="c3216-118">検索フォルダーのテンプレートの詳細については、 [[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3216-118">For more information about Search Folder Templates see [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c3216-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c3216-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c3216-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c3216-120">Protocol specifications</span></span>

<span data-ttu-id="c3216-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3216-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3216-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3216-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c3216-123">[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3216-123">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3216-124">プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c3216-124">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c3216-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c3216-125">Header files</span></span>

<span data-ttu-id="c3216-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c3216-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c3216-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3216-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c3216-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c3216-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c3216-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c3216-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3216-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="c3216-130">See also</span></span>



[<span data-ttu-id="c3216-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c3216-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c3216-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c3216-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c3216-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c3216-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c3216-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c3216-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

