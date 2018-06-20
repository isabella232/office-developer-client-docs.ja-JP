---
title: PidTagSearchFolderExpiration の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bd70d18242fadee964ad96305728e63617a0276f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803490"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="44047-103">PidTagSearchFolderExpiration の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="44047-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="44047-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44047-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44047-105">検索フォルダーのコンテナーを古くなっている、時間が含まれていて、更新または再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="44047-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44047-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="44047-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44047-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="44047-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="44047-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="44047-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44047-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="44047-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="44047-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="44047-110">Data type:</span></span>  <br/> |<span data-ttu-id="44047-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="44047-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="44047-112">領域:</span><span class="sxs-lookup"><span data-stu-id="44047-112">Area:</span></span>  <br/> |<span data-ttu-id="44047-113">検索</span><span class="sxs-lookup"><span data-stu-id="44047-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44047-114">備考</span><span class="sxs-lookup"><span data-stu-id="44047-114">Remarks</span></span>

<span data-ttu-id="44047-115">午前 0 時世界協定時刻 (UTC) 1601 年 1 月 1 日以降の分の数としては、このプロパティをフォーマットしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="44047-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="44047-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="44047-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="44047-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="44047-117">Protocol specifications</span></span>

<span data-ttu-id="44047-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44047-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44047-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="44047-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="44047-120">[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44047-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44047-121">プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="44047-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="44047-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="44047-122">Header files</span></span>

<span data-ttu-id="44047-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44047-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="44047-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="44047-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="44047-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="44047-125">Mapitags.h</span></span>
  
> <span data-ttu-id="44047-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="44047-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44047-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="44047-127">See also</span></span>



[<span data-ttu-id="44047-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="44047-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44047-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="44047-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44047-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="44047-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44047-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="44047-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

