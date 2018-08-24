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
ms.openlocfilehash: 1bdd8a283fead891261bbb05c38d398132870a50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582260"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a><span data-ttu-id="a806c-103">PidTagSearchFolderEfpFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a806c-103">PidTagSearchFolderEfpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="a806c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a806c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a806c-105">検索フォルダー検索フォルダーのコンテナーに適用される拡張フォルダーのフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a806c-105">Contains extended folder flags that apply to the search folder container for the search folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a806c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a806c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a806c-107">PR_WB_SF_EFP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a806c-107">PR_WB_SF_EFP_FLAGS</span></span>  <br/> |
|<span data-ttu-id="a806c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a806c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a806c-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="a806c-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="a806c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a806c-110">Data type:</span></span>  <br/> |<span data-ttu-id="a806c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a806c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a806c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a806c-112">Area:</span></span>  <br/> |<span data-ttu-id="a806c-113">検索</span><span class="sxs-lookup"><span data-stu-id="a806c-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a806c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a806c-114">Remarks</span></span>

<span data-ttu-id="a806c-115">このプロパティは、 **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) のプロパティ、および、 **ExtendedFlags**サブ b のプロパティ、フィールド、フォルダーの内のフラグを含める必要があります具体的には。</span><span class="sxs-lookup"><span data-stu-id="a806c-115">This property should specifically contain the flags in the **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) property, and the **ExtendedFlags** sub-property, in field b for the folder.</span></span> <span data-ttu-id="a806c-116">フォルダーのフラグに関する情報は、 [[MS OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a806c-116">For information about folder flags see the [[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a806c-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a806c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a806c-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a806c-118">Protocol specifications</span></span>

<span data-ttu-id="a806c-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a806c-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a806c-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a806c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a806c-121">[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a806c-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a806c-122">プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a806c-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
<span data-ttu-id="a806c-123">[[MS OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a806c-123">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a806c-124">場所と共有カテゴリのリストおよび作業時間など、クライアントとサーバーの構成データのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="a806c-124">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a806c-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a806c-125">Header files</span></span>

<span data-ttu-id="a806c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a806c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a806c-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a806c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a806c-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a806c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a806c-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a806c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a806c-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="a806c-130">See also</span></span>



[<span data-ttu-id="a806c-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a806c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a806c-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a806c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a806c-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a806c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a806c-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a806c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

