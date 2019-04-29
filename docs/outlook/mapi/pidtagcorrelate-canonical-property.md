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
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="dff5f-103">PidTagCorrelate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dff5f-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="dff5f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dff5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dff5f-105">メッセージの送信者がメッセージングシステムの相互関係機能を要求している場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dff5f-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dff5f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="dff5f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dff5f-107">PR_CORRELATE</span><span class="sxs-lookup"><span data-stu-id="dff5f-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="dff5f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="dff5f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dff5f-109">0x0e0c</span><span class="sxs-lookup"><span data-stu-id="dff5f-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="dff5f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="dff5f-110">Data type:</span></span>  <br/> |<span data-ttu-id="dff5f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="dff5f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="dff5f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="dff5f-112">Area:</span></span>  <br/> |<span data-ttu-id="dff5f-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="dff5f-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dff5f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="dff5f-114">Remarks</span></span>

<span data-ttu-id="dff5f-115">このプロパティは、受信レポートと元の送信されたメッセージの関連付けを要求するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="dff5f-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="dff5f-116">トランスポートプロバイダーは、 **PR_CORRELATE**が TRUE に設定された送信済みのメッセージを検出すると、 **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) プロパティをそのメッセージのメッセージ転送システム (MTS) 識別子に設定します。</span><span class="sxs-lookup"><span data-stu-id="dff5f-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="dff5f-117">**PR_CORRELATE**は、などの MTS 識別子による関連付けをサポートするメッセージングシステムで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dff5f-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dff5f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="dff5f-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="dff5f-119">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="dff5f-119">Header files</span></span>

<span data-ttu-id="dff5f-120">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dff5f-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="dff5f-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="dff5f-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="dff5f-122">Mapitags</span><span class="sxs-lookup"><span data-stu-id="dff5f-122">Mapitags.h</span></span>
  
> <span data-ttu-id="dff5f-123">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dff5f-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dff5f-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="dff5f-124">See also</span></span>



[<span data-ttu-id="dff5f-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="dff5f-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dff5f-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dff5f-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dff5f-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="dff5f-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dff5f-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="dff5f-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

