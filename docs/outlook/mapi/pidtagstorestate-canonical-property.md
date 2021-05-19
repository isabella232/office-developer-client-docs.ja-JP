---
title: PidTagStoreState 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreState
api_type:
- COM
ms.assetid: 36e49cf5-1411-42c5-9112-09958243996d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8f00addf7abdd765d97c54350e46979f788f06ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341154"
---
# <a name="pidtagstorestate-canonical-property"></a><span data-ttu-id="78424-103">PidTagStoreState 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="78424-103">PidTagStoreState Canonical Property</span></span>

  
  
<span data-ttu-id="78424-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78424-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78424-105">メッセージ ストアの状態を示すフラグが含まれる。</span><span class="sxs-lookup"><span data-stu-id="78424-105">Contains a flag that describes the state of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="78424-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="78424-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="78424-107">PR_STORE_STATE</span><span class="sxs-lookup"><span data-stu-id="78424-107">PR_STORE_STATE</span></span>  <br/> |
|<span data-ttu-id="78424-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="78424-108">Identifier:</span></span>  <br/> |<span data-ttu-id="78424-109">0x340E</span><span class="sxs-lookup"><span data-stu-id="78424-109">0x340E</span></span>  <br/> |
|<span data-ttu-id="78424-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="78424-110">Data type:</span></span>  <br/> |<span data-ttu-id="78424-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="78424-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="78424-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="78424-112">Area:</span></span>  <br/> |<span data-ttu-id="78424-113">MAPI メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="78424-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78424-114">注釈</span><span class="sxs-lookup"><span data-stu-id="78424-114">Remarks</span></span>

<span data-ttu-id="78424-115">このプロパティは動的で、ユーザーの操作に基づいて変更できます **(PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティとは異なる)。</span><span class="sxs-lookup"><span data-stu-id="78424-115">This property is dynamic and can change based on user actions, unlike the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="78424-116">次の値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="78424-116">The following value can be set:</span></span>
  
<span data-ttu-id="78424-117">STORE_HAS_SEARCHES</span><span class="sxs-lookup"><span data-stu-id="78424-117">STORE_HAS_SEARCHES</span></span> 
  
> <span data-ttu-id="78424-118">ユーザーがストア内に 1 つ以上のアクティブな検索を作成しました。</span><span class="sxs-lookup"><span data-stu-id="78424-118">The user has created one or more active searches in the store.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="78424-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="78424-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="78424-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="78424-120">Protocol specifications</span></span>

<span data-ttu-id="78424-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78424-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78424-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="78424-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="78424-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78424-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78424-124">コア メッセージ ストア オブジェクトに対して許容される操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="78424-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="78424-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="78424-125">Header files</span></span>

<span data-ttu-id="78424-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78424-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="78424-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="78424-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="78424-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="78424-128">Mapitags.h</span></span>
  
> <span data-ttu-id="78424-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="78424-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78424-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="78424-130">See also</span></span>



[<span data-ttu-id="78424-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="78424-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78424-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="78424-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78424-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="78424-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78424-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="78424-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

