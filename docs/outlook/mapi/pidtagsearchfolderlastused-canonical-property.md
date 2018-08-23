---
title: PidTagSearchFolderLastUsed 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderLastUsed
api_type:
- COM
ms.assetid: e4071307-6205-4079-ab65-7499d14f145c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cafa336bf915abd35de07a11ee65baf9ac4d69f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572691"
---
# <a name="pidtagsearchfolderlastused-canonical-property"></a><span data-ttu-id="03ab3-103">PidTagSearchFolderLastUsed 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="03ab3-103">PidTagSearchFolderLastUsed Canonical Property</span></span>

  
  
<span data-ttu-id="03ab3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03ab3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03ab3-105">フォルダーにアクセスした最後の時間を表します。</span><span class="sxs-lookup"><span data-stu-id="03ab3-105">Represents the last time the folder was accessed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03ab3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="03ab3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03ab3-107">PR_WB_SF_LAST_USED</span><span class="sxs-lookup"><span data-stu-id="03ab3-107">PR_WB_SF_LAST_USED</span></span>  <br/> |
|<span data-ttu-id="03ab3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="03ab3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03ab3-109">0x6834</span><span class="sxs-lookup"><span data-stu-id="03ab3-109">0x6834</span></span>  <br/> |
|<span data-ttu-id="03ab3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="03ab3-110">Data type:</span></span>  <br/> |<span data-ttu-id="03ab3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="03ab3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="03ab3-112">領域:</span><span class="sxs-lookup"><span data-stu-id="03ab3-112">Area:</span></span>  <br/> |<span data-ttu-id="03ab3-113">検索</span><span class="sxs-lookup"><span data-stu-id="03ab3-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03ab3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="03ab3-114">Remarks</span></span>

<span data-ttu-id="03ab3-115">午前 0 時世界協定時刻 (UTC) 1601 年 1 月 1 日以降の分の数としては、このプロパティをフォーマットしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="03ab3-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="03ab3-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="03ab3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03ab3-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="03ab3-117">Protocol specifications</span></span>

<span data-ttu-id="03ab3-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03ab3-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03ab3-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="03ab3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03ab3-120">[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03ab3-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03ab3-121">プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="03ab3-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03ab3-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="03ab3-122">Header files</span></span>

<span data-ttu-id="03ab3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03ab3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="03ab3-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="03ab3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="03ab3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="03ab3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="03ab3-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03ab3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03ab3-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="03ab3-127">See also</span></span>



[<span data-ttu-id="03ab3-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="03ab3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03ab3-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="03ab3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03ab3-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="03ab3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03ab3-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="03ab3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

