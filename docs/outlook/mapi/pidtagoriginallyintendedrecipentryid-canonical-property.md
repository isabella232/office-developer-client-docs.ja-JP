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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cf9a070e8f892cb7bd4668b3f92397070e5b2284
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430141"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a><span data-ttu-id="bd294-103">PidTagOriginallyIntendedRecipEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bd294-103">PidTagOriginallyIntendedRecipEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="bd294-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd294-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd294-105">自動転送されたメッセージの最初に意図された受信者のエントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="bd294-105">Contains the entry identifier of the originally intended recipient of an auto-forwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd294-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bd294-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd294-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bd294-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="bd294-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bd294-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bd294-109">0x1012</span><span class="sxs-lookup"><span data-stu-id="bd294-109">0x1012</span></span>  <br/> |
|<span data-ttu-id="bd294-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bd294-110">Data type:</span></span>  <br/> |<span data-ttu-id="bd294-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd294-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bd294-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bd294-112">Area:</span></span>  <br/> |<span data-ttu-id="bd294-113">Server</span><span class="sxs-lookup"><span data-stu-id="bd294-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd294-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bd294-114">Remarks</span></span>

<span data-ttu-id="bd294-115">このプロパティは、最初に意図したメッセージ受信者のアドレス プロパティの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="bd294-115">This property is one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="bd294-116">メッセージを転送した自動エージェントによって設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd294-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="bd294-117">このプロパティは、受信者ごとの X.400 レポート属性に対応します。</span><span class="sxs-lookup"><span data-stu-id="bd294-117">This property corresponds to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bd294-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bd294-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bd294-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bd294-119">Header files</span></span>

<span data-ttu-id="bd294-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd294-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd294-121">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bd294-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="bd294-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bd294-122">Mapitags.h</span></span>
  
> <span data-ttu-id="bd294-123">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="bd294-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd294-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd294-124">See also</span></span>



[<span data-ttu-id="bd294-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bd294-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd294-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bd294-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd294-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bd294-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd294-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bd294-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

