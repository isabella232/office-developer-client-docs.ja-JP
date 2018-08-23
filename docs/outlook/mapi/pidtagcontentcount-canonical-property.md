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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3c542b07eac626da5fbbb6a96b4545ad3c8558b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802618"
---
# <a name="pidtagcontentcount-canonical-property"></a><span data-ttu-id="838f8-103">PidTagContentCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="838f8-103">PidTagContentCount Canonical Property</span></span>

  
  
<span data-ttu-id="838f8-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="838f8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="838f8-105">メッセージ ・ ストアによって計算される、フォルダー内のメッセージの数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="838f8-105">Contains the number of messages in a folder, as computed by the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="838f8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="838f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="838f8-107">PR_CONTENT_COUNT</span><span class="sxs-lookup"><span data-stu-id="838f8-107">PR_CONTENT_COUNT</span></span>  <br/> |
|<span data-ttu-id="838f8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="838f8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="838f8-109">0x3602</span><span class="sxs-lookup"><span data-stu-id="838f8-109">0x3602</span></span>  <br/> |
|<span data-ttu-id="838f8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="838f8-110">Data type:</span></span>  <br/> |<span data-ttu-id="838f8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="838f8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="838f8-112">領域:</span><span class="sxs-lookup"><span data-stu-id="838f8-112">Area:</span></span>  <br/> |<span data-ttu-id="838f8-113">Folder</span><span class="sxs-lookup"><span data-stu-id="838f8-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="838f8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="838f8-114">Remarks</span></span>

<span data-ttu-id="838f8-115">関連は、目的が異なる、2 つのメッセージ ・ ストアによって計算されるこのプロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="838f8-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="838f8-116">MapiFolder オブジェクトでは、フォルダー内のメッセージの数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="838f8-116">On a MapiFolder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="838f8-117">カテゴリ別の MAPI テーブル内の見出し行には見出し行に対応するカテゴリに関連付けられているメッセージの数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="838f8-117">In a heading row in categorized MAPI tables, it contains the number of non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="838f8-118">このプロパティに含まれている番号では、フォルダーに関連付けられているエントリは含まれません。</span><span class="sxs-lookup"><span data-stu-id="838f8-118">The number contained in this property does not include associated entries in the folder.</span></span> <span data-ttu-id="838f8-119">**PR_CONTENT_UNREAD**([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) には、フォルダーの未読メ ッ セージの数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="838f8-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contains the count of unread messages for the folder.</span></span> <span data-ttu-id="838f8-120">クライアント アプリケーションは、読み取りが、このプロパティは、 **PR_CONTENT_UNREAD**を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="838f8-120">A client application can read but not change this property and **PR_CONTENT_UNREAD**.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="838f8-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="838f8-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="838f8-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="838f8-122">Protocol specifications</span></span>

<span data-ttu-id="838f8-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="838f8-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="838f8-124">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="838f8-124">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="838f8-125">[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="838f8-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="838f8-126">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="838f8-126">Handles folder operations.</span></span>
    
<span data-ttu-id="838f8-127">[[MS OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="838f8-127">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="838f8-128">テーブルのコア オブジェクトに許容される操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="838f8-128">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="838f8-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="838f8-129">Header files</span></span>

<span data-ttu-id="838f8-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="838f8-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="838f8-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="838f8-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="838f8-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="838f8-132">Mapitags.h</span></span>
  
> <span data-ttu-id="838f8-133">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="838f8-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="838f8-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="838f8-134">See also</span></span>



[<span data-ttu-id="838f8-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="838f8-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="838f8-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="838f8-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="838f8-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="838f8-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="838f8-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="838f8-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

