---
title: PidTagSearchFolderTag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: b7a88387-72ff-49e5-b73a-8bafab635658
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a4ad72c147abebfe9863d19690bc9f27f00544a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282321"
---
# <a name="pidtagsearchfoldertag-canonical-property"></a><span data-ttu-id="9ed68-103">PidTagSearchFolderTag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9ed68-103">PidTagSearchFolderTag Canonical Property</span></span>

  
  
<span data-ttu-id="9ed68-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ed68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ed68-105">この定義メッセージを一致する検索フォルダー コンテナーと同期するために使用される値を格納します。</span><span class="sxs-lookup"><span data-stu-id="9ed68-105">Contains the value used to synchronize this definition message with the matching search folder container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ed68-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9ed68-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ed68-107">PR_WB_SF_TAG</span><span class="sxs-lookup"><span data-stu-id="9ed68-107">PR_WB_SF_TAG</span></span>  <br/> |
|<span data-ttu-id="9ed68-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9ed68-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ed68-109">0x6847</span><span class="sxs-lookup"><span data-stu-id="9ed68-109">0x6847</span></span>  <br/> |
|<span data-ttu-id="9ed68-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9ed68-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ed68-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9ed68-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9ed68-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9ed68-112">Area:</span></span>  <br/> |<span data-ttu-id="9ed68-113">検索</span><span class="sxs-lookup"><span data-stu-id="9ed68-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ed68-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9ed68-114">Remarks</span></span>

<span data-ttu-id="9ed68-115">このプロパティは、定義メッセージが変更された場合に変更されます。</span><span class="sxs-lookup"><span data-stu-id="9ed68-115">This property is changed when the definition message is changed.</span></span> <span data-ttu-id="9ed68-116">繰り返しごとに変更する必要がありますが、一意ではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="9ed68-116">It must change each iteration, but it may not be unique.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9ed68-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9ed68-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ed68-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9ed68-118">Protocol specifications</span></span>

<span data-ttu-id="9ed68-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ed68-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ed68-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="9ed68-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ed68-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ed68-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ed68-122">検索フォルダー 一覧の構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9ed68-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ed68-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9ed68-123">Header files</span></span>

<span data-ttu-id="9ed68-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ed68-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ed68-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9ed68-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ed68-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9ed68-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9ed68-127">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="9ed68-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ed68-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9ed68-128">See also</span></span>



[<span data-ttu-id="9ed68-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9ed68-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ed68-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9ed68-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ed68-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9ed68-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ed68-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9ed68-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

