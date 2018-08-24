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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 063e41bf9fe306b3862e302abb4495ca56e3087b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575456"
---
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="baad9-103">PidTagCorrelate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="baad9-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="baad9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="baad9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="baad9-105">メッセージの送信者のメッセージング システムの相互関係の機能を要求する場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="baad9-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="baad9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="baad9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="baad9-107">PR_CORRELATE</span><span class="sxs-lookup"><span data-stu-id="baad9-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="baad9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="baad9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="baad9-109">0x0E0C</span><span class="sxs-lookup"><span data-stu-id="baad9-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="baad9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="baad9-110">Data type:</span></span>  <br/> |<span data-ttu-id="baad9-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="baad9-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="baad9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="baad9-112">Area:</span></span>  <br/> |<span data-ttu-id="baad9-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="baad9-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="baad9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="baad9-114">Remarks</span></span>

<span data-ttu-id="baad9-115">元の送信メッセージと受信したレポートの相関関係を要求するこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="baad9-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="baad9-116">トランスポート プロバイダーでは、true を指定する**PR_CORRELATE**のセットを使用して発信されたメッセージが検出されると、そのメッセージのメッセージ転送システム (MTS) 識別子を**PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="baad9-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="baad9-117">X.400 など、MTS の id では、メッセージの相関関係をサポートしているシステムで**PR_CORRELATE**を使用してください。</span><span class="sxs-lookup"><span data-stu-id="baad9-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="baad9-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="baad9-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="baad9-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="baad9-119">Header files</span></span>

<span data-ttu-id="baad9-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="baad9-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="baad9-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="baad9-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="baad9-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="baad9-122">Mapitags.h</span></span>
  
> <span data-ttu-id="baad9-123">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="baad9-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="baad9-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="baad9-124">See also</span></span>



[<span data-ttu-id="baad9-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="baad9-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="baad9-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="baad9-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="baad9-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="baad9-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="baad9-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="baad9-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

