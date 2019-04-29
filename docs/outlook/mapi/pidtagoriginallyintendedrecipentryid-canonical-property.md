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
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a><span data-ttu-id="36f35-103">PidTagOriginallyIntendedRecipEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="36f35-103">PidTagOriginallyIntendedRecipEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="36f35-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36f35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36f35-105">自動転送されたメッセージの最初に意図した受信者のエントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="36f35-105">Contains the entry identifier of the originally intended recipient of an auto-forwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36f35-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="36f35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="36f35-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="36f35-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="36f35-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="36f35-108">Identifier:</span></span>  <br/> |<span data-ttu-id="36f35-109">0x1012</span><span class="sxs-lookup"><span data-stu-id="36f35-109">0x1012</span></span>  <br/> |
|<span data-ttu-id="36f35-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="36f35-110">Data type:</span></span>  <br/> |<span data-ttu-id="36f35-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="36f35-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="36f35-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="36f35-112">Area:</span></span>  <br/> |<span data-ttu-id="36f35-113">サーバー</span><span class="sxs-lookup"><span data-stu-id="36f35-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36f35-114">注釈</span><span class="sxs-lookup"><span data-stu-id="36f35-114">Remarks</span></span>

<span data-ttu-id="36f35-115">このプロパティは、最初に意図したメッセージ受信者のアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="36f35-115">This property is one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="36f35-116">メッセージを転送した自動エージェントによって設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="36f35-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="36f35-117">このプロパティは、受信者ごとの-400 レポート属性に対応します。</span><span class="sxs-lookup"><span data-stu-id="36f35-117">This property corresponds to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="36f35-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="36f35-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="36f35-119">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="36f35-119">Header files</span></span>

<span data-ttu-id="36f35-120">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="36f35-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="36f35-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="36f35-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="36f35-122">Mapitags</span><span class="sxs-lookup"><span data-stu-id="36f35-122">Mapitags.h</span></span>
  
> <span data-ttu-id="36f35-123">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="36f35-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36f35-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="36f35-124">See also</span></span>



[<span data-ttu-id="36f35-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="36f35-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="36f35-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="36f35-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="36f35-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="36f35-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="36f35-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="36f35-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

