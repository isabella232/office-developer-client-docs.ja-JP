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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 41aa97a52176cf68775d6fd507d3d042888092cc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393860"
---
# <a name="pidtagswappedtodostore-canonical-property"></a><span data-ttu-id="7c0e4-103">PidTagSwappedToDoStore 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7c0e4-103">PidTagSwappedToDoStore Canonical Property</span></span>

  
  
<span data-ttu-id="7c0e4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c0e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c0e4-105">必要性を決定するの転送、電子メールの処理後です。</span><span class="sxs-lookup"><span data-stu-id="7c0e4-105">Determines the need for post-transmit processing of an email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c0e4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7c0e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c0e4-107">PR_SWAPPED_TODO_STORE</span><span class="sxs-lookup"><span data-stu-id="7c0e4-107">PR_SWAPPED_TODO_STORE</span></span>  <br/> |
|<span data-ttu-id="7c0e4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7c0e4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c0e4-109">0x0E2C</span><span class="sxs-lookup"><span data-stu-id="7c0e4-109">0x0E2C</span></span>  <br/> |
|<span data-ttu-id="7c0e4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7c0e4-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c0e4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7c0e4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7c0e4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7c0e4-112">Area:</span></span>  <br/> |<span data-ttu-id="7c0e4-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="7c0e4-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c0e4-114">備考</span><span class="sxs-lookup"><span data-stu-id="7c0e4-114">Remarks</span></span>

<span data-ttu-id="7c0e4-115">下書きメッセージにこのプロパティが設定されている場合は、メッセージの**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) のプロパティの値にその値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c0e4-115">If this property is set on a draft message, then its value must be set to the value of **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property of the message.</span></span>
  
<span data-ttu-id="7c0e4-116">詳細については、 [[MS OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)を参照してくださいセクション"送信後フラグ付きメッセージの処理します」。</span><span class="sxs-lookup"><span data-stu-id="7c0e4-116">For more information, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section "Post-Transmit Processing of a Flagged Message."</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7c0e4-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7c0e4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c0e4-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7c0e4-118">Protocol specifications</span></span>

<span data-ttu-id="7c0e4-119">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c0e4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c0e4-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7c0e4-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c0e4-121">[[MS OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c0e4-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c0e4-122">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7c0e4-122">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="7c0e4-123">[[MS OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c0e4-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c0e4-124">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="7c0e4-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c0e4-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7c0e4-125">Header files</span></span>

<span data-ttu-id="7c0e4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c0e4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c0e4-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7c0e4-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c0e4-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7c0e4-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7c0e4-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c0e4-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c0e4-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c0e4-130">See also</span></span>



[<span data-ttu-id="7c0e4-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7c0e4-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c0e4-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7c0e4-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c0e4-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7c0e4-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c0e4-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7c0e4-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

