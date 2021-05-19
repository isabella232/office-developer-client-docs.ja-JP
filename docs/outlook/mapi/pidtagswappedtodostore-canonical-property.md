---
title: PidTagSwappedToDoStore 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoStore
api_type:
- COM
ms.assetid: 1edae9ac-fc9a-4bfe-b053-99de848c5144
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 41aa97a52176cf68775d6fd507d3d042888092cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358906"
---
# <a name="pidtagswappedtodostore-canonical-property"></a><span data-ttu-id="bae56-103">PidTagSwappedToDoStore 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bae56-103">PidTagSwappedToDoStore Canonical Property</span></span>

  
  
<span data-ttu-id="bae56-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bae56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bae56-105">電子メールの送信後処理の必要性を決定します。</span><span class="sxs-lookup"><span data-stu-id="bae56-105">Determines the need for post-transmit processing of an email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bae56-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bae56-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bae56-107">PR_SWAPPED_TODO_STORE</span><span class="sxs-lookup"><span data-stu-id="bae56-107">PR_SWAPPED_TODO_STORE</span></span>  <br/> |
|<span data-ttu-id="bae56-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bae56-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bae56-109">0x0E2C</span><span class="sxs-lookup"><span data-stu-id="bae56-109">0x0E2C</span></span>  <br/> |
|<span data-ttu-id="bae56-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bae56-110">Data type:</span></span>  <br/> |<span data-ttu-id="bae56-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bae56-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bae56-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bae56-112">Area:</span></span>  <br/> |<span data-ttu-id="bae56-113">MAPI 送信不可</span><span class="sxs-lookup"><span data-stu-id="bae56-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bae56-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bae56-114">Remarks</span></span>

<span data-ttu-id="bae56-115">このプロパティが下書きメッセージに設定されている場合、その値はメッセージの **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) プロパティの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bae56-115">If this property is set on a draft message, then its value must be set to the value of **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property of the message.</span></span>
  
<span data-ttu-id="bae56-116">詳細については [、「[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) 」セクション「フラグが設定されたメッセージの送信後処理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bae56-116">For more information, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section "Post-Transmit Processing of a Flagged Message."</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bae56-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bae56-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bae56-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bae56-118">Protocol specifications</span></span>

<span data-ttu-id="bae56-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bae56-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bae56-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="bae56-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bae56-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bae56-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bae56-122">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bae56-122">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="bae56-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bae56-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bae56-124">メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="bae56-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bae56-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bae56-125">Header files</span></span>

<span data-ttu-id="bae56-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bae56-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bae56-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bae56-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="bae56-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bae56-128">Mapitags.h</span></span>
  
> <span data-ttu-id="bae56-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="bae56-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bae56-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="bae56-130">See also</span></span>



[<span data-ttu-id="bae56-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bae56-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bae56-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bae56-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bae56-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bae56-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bae56-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bae56-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

