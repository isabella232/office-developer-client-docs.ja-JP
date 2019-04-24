---
title: PidTagSearchFolderEfpFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderEfpFlags
api_type:
- COM
ms.assetid: ef82a75f-a09f-4880-ba6a-e739b16422a3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d670aa91cc60c051f8464f9d83536b888b44ca9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336429"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a><span data-ttu-id="fb286-103">PidTagSearchFolderEfpFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fb286-103">PidTagSearchFolderEfpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="fb286-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb286-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb286-105">検索フォルダーの検索フォルダーコンテナーに適用する拡張フォルダーフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fb286-105">Contains extended folder flags that apply to the search folder container for the search folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fb286-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fb286-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fb286-107">PR_WB_SF_EFP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="fb286-107">PR_WB_SF_EFP_FLAGS</span></span>  <br/> |
|<span data-ttu-id="fb286-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fb286-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fb286-109">0x684 8</span><span class="sxs-lookup"><span data-stu-id="fb286-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="fb286-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fb286-110">Data type:</span></span>  <br/> |<span data-ttu-id="fb286-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fb286-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fb286-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="fb286-112">Area:</span></span>  <br/> |<span data-ttu-id="fb286-113">検索</span><span class="sxs-lookup"><span data-stu-id="fb286-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb286-114">解説</span><span class="sxs-lookup"><span data-stu-id="fb286-114">Remarks</span></span>

<span data-ttu-id="fb286-115">このプロパティには、フォルダーのフィールド b に、 **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) プロパティと**extendedflags**サブプロパティのフラグが明示的に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb286-115">This property should specifically contain the flags in the **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) property, and the **ExtendedFlags** sub-property, in field b for the folder.</span></span> <span data-ttu-id="fb286-116">フォルダーフラグの詳細については、 [[OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb286-116">For information about folder flags see the [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fb286-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fb286-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fb286-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fb286-118">Protocol specifications</span></span>

<span data-ttu-id="fb286-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb286-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb286-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fb286-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fb286-121">[[OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb286-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb286-122">検索フォルダーリストの構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="fb286-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
<span data-ttu-id="fb286-123">[[OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb286-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb286-124">カテゴリの共有リストや稼働時間など、クライアントおよびサーバーの構成データの場所とプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="fb286-124">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fb286-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="fb286-125">Header files</span></span>

<span data-ttu-id="fb286-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb286-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fb286-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fb286-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="fb286-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="fb286-128">Mapitags.h</span></span>
  
> <span data-ttu-id="fb286-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fb286-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb286-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="fb286-130">See also</span></span>



[<span data-ttu-id="fb286-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fb286-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fb286-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fb286-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fb286-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fb286-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fb286-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fb286-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

