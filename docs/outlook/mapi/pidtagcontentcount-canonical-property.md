---
title: PidTagContentCount 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCount
api_type:
- HeaderDef
ms.assetid: 27c75031-a968-4636-98a6-4a5b7422f57c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e9994da72bbc38a546f220e5ecf8768b80c6f1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331956"
---
# <a name="pidtagcontentcount-canonical-property"></a><span data-ttu-id="ecd0d-103">PidTagContentCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ecd0d-103">PidTagContentCount Canonical Property</span></span>

  
  
<span data-ttu-id="ecd0d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecd0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecd0d-105">メッセージ ストアによって計算されるフォルダー内のメッセージの数を格納します。</span><span class="sxs-lookup"><span data-stu-id="ecd0d-105">Contains the number of messages in a folder, as computed by the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ecd0d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ecd0d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ecd0d-107">PR_CONTENT_COUNT</span><span class="sxs-lookup"><span data-stu-id="ecd0d-107">PR_CONTENT_COUNT</span></span>  <br/> |
|<span data-ttu-id="ecd0d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ecd0d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ecd0d-109">0x3602</span><span class="sxs-lookup"><span data-stu-id="ecd0d-109">0x3602</span></span>  <br/> |
|<span data-ttu-id="ecd0d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ecd0d-110">Data type:</span></span>  <br/> |<span data-ttu-id="ecd0d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ecd0d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ecd0d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ecd0d-112">Area:</span></span>  <br/> |<span data-ttu-id="ecd0d-113">Folder</span><span class="sxs-lookup"><span data-stu-id="ecd0d-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecd0d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ecd0d-114">Remarks</span></span>

<span data-ttu-id="ecd0d-115">メッセージ ストアによって計算されるこのプロパティは、関連する 2 つの異なる目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="ecd0d-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="ecd0d-116">MapiFolder オブジェクトには、フォルダー内のメッセージの数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ecd0d-116">On a MapiFolder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="ecd0d-117">分類された MAPI テーブルの見出し行には、その見出し行に対応するカテゴリ内の関連付けされていないメッセージの数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ecd0d-117">In a heading row in categorized MAPI tables, it contains the number of non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="ecd0d-118">このプロパティに含まれる番号には、フォルダーに関連付けられたエントリは含めされません。</span><span class="sxs-lookup"><span data-stu-id="ecd0d-118">The number contained in this property does not include associated entries in the folder.</span></span> <span data-ttu-id="ecd0d-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) には、フォルダーの未読メッセージの数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ecd0d-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contains the count of unread messages for the folder.</span></span> <span data-ttu-id="ecd0d-120">クライアント アプリケーションは、このプロパティとプロパティを読み取り、変更 **PR_CONTENT_UNREAD。**</span><span class="sxs-lookup"><span data-stu-id="ecd0d-120">A client application can read but not change this property and **PR_CONTENT_UNREAD**.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ecd0d-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ecd0d-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ecd0d-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ecd0d-122">Protocol specifications</span></span>

<span data-ttu-id="ecd0d-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecd0d-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecd0d-124">関連するプロトコル仕様へのMicrosoft Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="ecd0d-124">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ecd0d-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecd0d-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecd0d-126">フォルダー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="ecd0d-126">Handles folder operations.</span></span>
    
<span data-ttu-id="ecd0d-127">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecd0d-127">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecd0d-128">コア テーブル オブジェクトに対して許容される操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ecd0d-128">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ecd0d-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ecd0d-129">Header files</span></span>

<span data-ttu-id="ecd0d-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecd0d-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="ecd0d-131">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ecd0d-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="ecd0d-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ecd0d-132">Mapitags.h</span></span>
  
> <span data-ttu-id="ecd0d-133">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="ecd0d-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecd0d-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="ecd0d-134">See also</span></span>



[<span data-ttu-id="ecd0d-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ecd0d-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ecd0d-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ecd0d-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ecd0d-137">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ecd0d-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ecd0d-138">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ecd0d-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

