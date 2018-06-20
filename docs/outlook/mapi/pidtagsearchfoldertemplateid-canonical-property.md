---
title: PidTagSearchFolderTemplateId の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4e752d3264a64ad7b467947c44d01eb7c47ec863
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803503"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a><span data-ttu-id="b057a-103">PidTagSearchFolderTemplateId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b057a-103">PidTagSearchFolderTemplateId Canonical Property</span></span>

  
  
<span data-ttu-id="b057a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b057a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b057a-105">検索に使用されているテンプレートの ID が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b057a-105">Contains the ID of the template that is being used for the search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b057a-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b057a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b057a-107">PR_WB_SF_TEMPLATE_ID</span><span class="sxs-lookup"><span data-stu-id="b057a-107">PR_WB_SF_TEMPLATE_ID</span></span>  <br/> |
|<span data-ttu-id="b057a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b057a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b057a-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="b057a-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="b057a-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="b057a-110">Data type:</span></span>  <br/> |<span data-ttu-id="b057a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b057a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b057a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b057a-112">Area:</span></span>  <br/> |<span data-ttu-id="b057a-113">検索</span><span class="sxs-lookup"><span data-stu-id="b057a-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b057a-114">備考</span><span class="sxs-lookup"><span data-stu-id="b057a-114">Remarks</span></span>

<span data-ttu-id="b057a-115">検索フォルダーの条件は、テンプレートによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="b057a-115">Search folder criteria is specified by a template.</span></span> <span data-ttu-id="b057a-116">検索フォルダーを定義するメッセージには、このプロパティは、対応するテンプレートを識別します。</span><span class="sxs-lookup"><span data-stu-id="b057a-116">This property on the message that defines the search folder identifies its corresponding template.</span></span> <span data-ttu-id="b057a-117">検索条件を定義するには、テンプレートも検索から除外するフォルダーを定義、検索から除外する項目を定義および**PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b057a-117">In addition to defining search criteria, a template also defines folders to exclude from the search, defines items to exclude from the search, and specifies the value of **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span></span>
  
<span data-ttu-id="b057a-118">検索フォルダーのテンプレートの詳細については、 [[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b057a-118">For more information about Search Folder Templates see [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b057a-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b057a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b057a-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b057a-120">Protocol specifications</span></span>

<span data-ttu-id="b057a-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b057a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b057a-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b057a-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b057a-123">[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b057a-123">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b057a-124">プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b057a-124">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b057a-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b057a-125">Header files</span></span>

<span data-ttu-id="b057a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b057a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b057a-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b057a-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b057a-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b057a-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b057a-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b057a-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b057a-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="b057a-130">See also</span></span>



[<span data-ttu-id="b057a-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b057a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b057a-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b057a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b057a-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="b057a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b057a-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="b057a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

