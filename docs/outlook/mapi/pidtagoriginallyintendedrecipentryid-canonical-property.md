---
title: PidTagOriginallyIntendedRecipEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEntryId
api_type:
- COM
ms.assetid: fc288a7a-1927-484e-b860-9cc118672ed2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4e7d97f4b2043c9ca08e487e52d58fb534c7abef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572656"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a><span data-ttu-id="4364b-103">PidTagOriginallyIntendedRecipEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4364b-103">PidTagOriginallyIntendedRecipEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="4364b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4364b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4364b-105">自動転送メッセージの最初の目的の受信者のエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4364b-105">Contains the entry identifier of the originally intended recipient of an auto-forwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4364b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4364b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4364b-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4364b-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="4364b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4364b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4364b-109">0x1012</span><span class="sxs-lookup"><span data-stu-id="4364b-109">0x1012</span></span>  <br/> |
|<span data-ttu-id="4364b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4364b-110">Data type:</span></span>  <br/> |<span data-ttu-id="4364b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4364b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4364b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4364b-112">Area:</span></span>  <br/> |<span data-ttu-id="4364b-113">Server</span><span class="sxs-lookup"><span data-stu-id="4364b-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4364b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4364b-114">Remarks</span></span>

<span data-ttu-id="4364b-115">このプロパティは、本来意図されているメッセージの受信者のアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="4364b-115">This property is one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="4364b-116">メッセージを転送するには、自動でエージェントを設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4364b-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="4364b-117">このプロパティは、レポートの X.400 受信者ごとの属性に対応します。</span><span class="sxs-lookup"><span data-stu-id="4364b-117">This property corresponds to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4364b-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4364b-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4364b-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4364b-119">Header files</span></span>

<span data-ttu-id="4364b-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4364b-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="4364b-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4364b-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="4364b-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4364b-122">Mapitags.h</span></span>
  
> <span data-ttu-id="4364b-123">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4364b-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4364b-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="4364b-124">See also</span></span>



[<span data-ttu-id="4364b-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4364b-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4364b-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4364b-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4364b-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4364b-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4364b-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4364b-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

