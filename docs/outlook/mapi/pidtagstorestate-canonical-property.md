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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7348d0395952036ee6b356b013072324b64e4b98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570822"
---
# <a name="pidtagstorestate-canonical-property"></a><span data-ttu-id="6b923-103">PidTagStoreState 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b923-103">PidTagStoreState Canonical Property</span></span>

  
  
<span data-ttu-id="6b923-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b923-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b923-105">メッセージ ・ ストアの状態を記述するフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6b923-105">Contains a flag that describes the state of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b923-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6b923-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6b923-107">PR_STORE_STATE</span><span class="sxs-lookup"><span data-stu-id="6b923-107">PR_STORE_STATE</span></span>  <br/> |
|<span data-ttu-id="6b923-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6b923-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6b923-109">0x340E</span><span class="sxs-lookup"><span data-stu-id="6b923-109">0x340E</span></span>  <br/> |
|<span data-ttu-id="6b923-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6b923-110">Data type:</span></span>  <br/> |<span data-ttu-id="6b923-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6b923-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6b923-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6b923-112">Area:</span></span>  <br/> |<span data-ttu-id="6b923-113">MAPI メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="6b923-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b923-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6b923-114">Remarks</span></span>

<span data-ttu-id="6b923-115">このプロパティは動的であり、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティとは異なり、ユーザーの操作に基づいて変更できます。</span><span class="sxs-lookup"><span data-stu-id="6b923-115">This property is dynamic and can change based on user actions, unlike the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="6b923-116">次の値を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="6b923-116">The following value can be set:</span></span>
  
<span data-ttu-id="6b923-117">STORE_HAS_SEARCHES</span><span class="sxs-lookup"><span data-stu-id="6b923-117">STORE_HAS_SEARCHES</span></span> 
  
> <span data-ttu-id="6b923-118">ユーザーがストアに 1 つまたは複数のアクティブな検索条件を作成します。</span><span class="sxs-lookup"><span data-stu-id="6b923-118">The user has created one or more active searches in the store.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="6b923-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6b923-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6b923-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6b923-120">Protocol specifications</span></span>

<span data-ttu-id="6b923-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b923-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b923-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6b923-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6b923-123">[[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b923-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b923-124">コア メッセージのストア オブジェクトの許可された操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b923-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6b923-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6b923-125">Header files</span></span>

<span data-ttu-id="6b923-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b923-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6b923-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6b923-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="6b923-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6b923-128">Mapitags.h</span></span>
  
> <span data-ttu-id="6b923-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6b923-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6b923-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b923-130">See also</span></span>



[<span data-ttu-id="6b923-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b923-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6b923-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b923-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6b923-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6b923-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6b923-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6b923-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

