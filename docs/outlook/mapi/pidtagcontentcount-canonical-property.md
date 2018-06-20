---
title: PidTagContentCount の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3c542b07eac626da5fbbb6a96b4545ad3c8558b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802618"
---
# <a name="pidtagcontentcount-canonical-property"></a><span data-ttu-id="3f3e4-103">PidTagContentCount の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="3f3e4-103">PidTagContentCount Canonical Property</span></span>

  
  
<span data-ttu-id="3f3e4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3f3e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3f3e4-105">メッセージ ・ ストアによって計算される、フォルダー内のメッセージの数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-105">Contains the number of messages in a folder, as computed by the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f3e4-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3f3e4-107">PR_CONTENT_COUNT</span><span class="sxs-lookup"><span data-stu-id="3f3e4-107">PR_CONTENT_COUNT</span></span>  <br/> |
|<span data-ttu-id="3f3e4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3f3e4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3f3e4-109">0x3602</span><span class="sxs-lookup"><span data-stu-id="3f3e4-109">0x3602</span></span>  <br/> |
|<span data-ttu-id="3f3e4-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-110">Data type:</span></span>  <br/> |<span data-ttu-id="3f3e4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3f3e4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3f3e4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="3f3e4-112">Area:</span></span>  <br/> |<span data-ttu-id="3f3e4-113">Folder</span><span class="sxs-lookup"><span data-stu-id="3f3e4-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f3e4-114">備考</span><span class="sxs-lookup"><span data-stu-id="3f3e4-114">Remarks</span></span>

<span data-ttu-id="3f3e4-115">関連は、目的が異なる、2 つのメッセージ ・ ストアによって計算されるこのプロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="3f3e4-116">MapiFolder オブジェクトでは、フォルダー内のメッセージの数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-116">On a MapiFolder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="3f3e4-117">カテゴリ別の MAPI テーブル内の見出し行には見出し行に対応するカテゴリに関連付けられているメッセージの数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-117">In a heading row in categorized MAPI tables, it contains the number of non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="3f3e4-118">このプロパティに含まれている番号では、フォルダーに関連付けられているエントリは含まれません。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-118">The number contained in this property does not include associated entries in the folder.</span></span> <span data-ttu-id="3f3e4-119">**PR_CONTENT_UNREAD**([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) には、フォルダーの未読メ ッ セージの数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contains the count of unread messages for the folder.</span></span> <span data-ttu-id="3f3e4-120">クライアント アプリケーションは、読み取りが、このプロパティは、 **PR_CONTENT_UNREAD**を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-120">A client application can read but not change this property and **PR_CONTENT_UNREAD**.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3f3e4-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3f3e4-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3f3e4-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3f3e4-122">Protocol specifications</span></span>

<span data-ttu-id="3f3e4-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f3e4-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f3e4-124">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-124">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3f3e4-125">[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f3e4-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f3e4-126">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-126">Handles folder operations.</span></span>
    
<span data-ttu-id="3f3e4-127">[[MS OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f3e4-127">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f3e4-128">テーブルのコア オブジェクトに許容される操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-128">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3f3e4-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3f3e4-129">Header files</span></span>

<span data-ttu-id="3f3e4-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f3e4-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="3f3e4-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="3f3e4-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3f3e4-132">Mapitags.h</span></span>
  
> <span data-ttu-id="3f3e4-133">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3f3e4-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="3f3e4-134">See also</span></span>



[<span data-ttu-id="3f3e4-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3f3e4-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3f3e4-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3f3e4-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3f3e4-137">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="3f3e4-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3f3e4-138">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="3f3e4-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

