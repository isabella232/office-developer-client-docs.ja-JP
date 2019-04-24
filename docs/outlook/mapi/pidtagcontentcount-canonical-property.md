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
ms.openlocfilehash: 7e9994da72bbc38a546f220e5ecf8768b80c6f1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331956"
---
# <a name="pidtagcontentcount-canonical-property"></a><span data-ttu-id="05354-103">PidTagContentCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="05354-103">PidTagContentCount Canonical Property</span></span>

  
  
<span data-ttu-id="05354-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05354-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05354-105">メッセージストアによって計算された、フォルダー内のメッセージの数を含みます。</span><span class="sxs-lookup"><span data-stu-id="05354-105">Contains the number of messages in a folder, as computed by the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05354-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="05354-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05354-107">PR_CONTENT_COUNT</span><span class="sxs-lookup"><span data-stu-id="05354-107">PR_CONTENT_COUNT</span></span>  <br/> |
|<span data-ttu-id="05354-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="05354-108">Identifier:</span></span>  <br/> |<span data-ttu-id="05354-109">0x3602</span><span class="sxs-lookup"><span data-stu-id="05354-109">0x3602</span></span>  <br/> |
|<span data-ttu-id="05354-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="05354-110">Data type:</span></span>  <br/> |<span data-ttu-id="05354-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="05354-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="05354-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="05354-112">Area:</span></span>  <br/> |<span data-ttu-id="05354-113">フォルダー</span><span class="sxs-lookup"><span data-stu-id="05354-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05354-114">解説</span><span class="sxs-lookup"><span data-stu-id="05354-114">Remarks</span></span>

<span data-ttu-id="05354-115">メッセージストアによって計算されたこのプロパティは、関連する2つの異なる目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="05354-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="05354-116">MapiFolder オブジェクトには、フォルダー内のメッセージの数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="05354-116">On a MapiFolder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="05354-117">カテゴリに分類された MAPI テーブルの見出し行には、その見出し行に対応するカテゴリに関連付けられていないメッセージの数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="05354-117">In a heading row in categorized MAPI tables, it contains the number of non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="05354-118">このプロパティに含まれる番号には、フォルダー内の関連付けられたエントリは含まれません。</span><span class="sxs-lookup"><span data-stu-id="05354-118">The number contained in this property does not include associated entries in the folder.</span></span> <span data-ttu-id="05354-119">**PR_CONTENT_UNREAD**([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) フォルダーの未読メッセージ数を含みます。</span><span class="sxs-lookup"><span data-stu-id="05354-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contains the count of unread messages for the folder.</span></span> <span data-ttu-id="05354-120">クライアントアプリケーションは、このプロパティと**PR_CONTENT_UNREAD**を読み取ることはできますが、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="05354-120">A client application can read but not change this property and **PR_CONTENT_UNREAD**.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="05354-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="05354-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05354-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="05354-122">Protocol specifications</span></span>

<span data-ttu-id="05354-123">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05354-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05354-124">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="05354-124">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="05354-125">[[OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05354-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05354-126">フォルダー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="05354-126">Handles folder operations.</span></span>
    
<span data-ttu-id="05354-127">[[OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05354-127">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05354-128">コアテーブルオブジェクトの許容可能な操作が含まれています。</span><span class="sxs-lookup"><span data-stu-id="05354-128">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05354-129">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="05354-129">Header files</span></span>

<span data-ttu-id="05354-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05354-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="05354-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="05354-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="05354-132">Mapitags</span><span class="sxs-lookup"><span data-stu-id="05354-132">Mapitags.h</span></span>
  
> <span data-ttu-id="05354-133">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="05354-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05354-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="05354-134">See also</span></span>



[<span data-ttu-id="05354-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="05354-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05354-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="05354-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05354-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="05354-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05354-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="05354-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

