---
title: PidTagSearchFolderExpiration 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderExpiration
api_type:
- COM
ms.assetid: e5746090-c850-4e95-b1e7-a07e42c87179
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a119bb735f752719d292371d4dc43e72450b33c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336471"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="f033b-103">PidTagSearchFolderExpiration 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f033b-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="f033b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f033b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f033b-105">検索フォルダー コンテナーが古い時間を含み、更新または再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f033b-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f033b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f033b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f033b-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="f033b-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="f033b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f033b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f033b-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="f033b-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="f033b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f033b-110">Data type:</span></span>  <br/> |<span data-ttu-id="f033b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f033b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f033b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f033b-112">Area:</span></span>  <br/> |<span data-ttu-id="f033b-113">検索</span><span class="sxs-lookup"><span data-stu-id="f033b-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f033b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f033b-114">Remarks</span></span>

<span data-ttu-id="f033b-115">このプロパティは、1601 年 1 月 1 日午前 0 時 (UTC) 以降の分数として書式設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f033b-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f033b-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f033b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f033b-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f033b-117">Protocol specifications</span></span>

<span data-ttu-id="f033b-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f033b-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f033b-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="f033b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f033b-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f033b-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f033b-121">検索フォルダー 一覧の構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f033b-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f033b-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f033b-122">Header files</span></span>

<span data-ttu-id="f033b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f033b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f033b-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f033b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f033b-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f033b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f033b-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f033b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f033b-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="f033b-127">See also</span></span>



[<span data-ttu-id="f033b-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f033b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f033b-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f033b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f033b-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f033b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f033b-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f033b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

