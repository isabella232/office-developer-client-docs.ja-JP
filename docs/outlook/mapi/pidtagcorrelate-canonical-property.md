---
title: PidTagCorrelate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ea217808a163c7f16bbaa3c5a959fd32c8cbe10c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405220"
---
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="8aff3-103">PidTagCorrelate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8aff3-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="8aff3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8aff3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8aff3-105">メッセージの送信者がメッセージング システムの相関機能を要求する場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="8aff3-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8aff3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8aff3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8aff3-107">PR_CORRELATE</span><span class="sxs-lookup"><span data-stu-id="8aff3-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="8aff3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8aff3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8aff3-109">0x0E0C</span><span class="sxs-lookup"><span data-stu-id="8aff3-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="8aff3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8aff3-110">Data type:</span></span>  <br/> |<span data-ttu-id="8aff3-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8aff3-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8aff3-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8aff3-112">Area:</span></span>  <br/> |<span data-ttu-id="8aff3-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="8aff3-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8aff3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8aff3-114">Remarks</span></span>

<span data-ttu-id="8aff3-115">このプロパティは、受信レポートと元の送信メッセージとの相関関係を要求するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8aff3-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="8aff3-116">トランスポート プロバイダーは **、PR_CORRELATE** が TRUE に設定された送信済みメッセージを検出すると **、PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) プロパティをそのメッセージのメッセージ転送システム (MTS) 識別子に設定します。</span><span class="sxs-lookup"><span data-stu-id="8aff3-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="8aff3-117"> PR_CORRELATE、X.400 などの MTS 識別子による相関関係をサポートするメッセージング システムで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8aff3-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8aff3-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8aff3-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8aff3-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8aff3-119">Header files</span></span>

<span data-ttu-id="8aff3-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8aff3-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="8aff3-121">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8aff3-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="8aff3-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8aff3-122">Mapitags.h</span></span>
  
> <span data-ttu-id="8aff3-123">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="8aff3-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8aff3-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="8aff3-124">See also</span></span>



[<span data-ttu-id="8aff3-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8aff3-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8aff3-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8aff3-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8aff3-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8aff3-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8aff3-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8aff3-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

