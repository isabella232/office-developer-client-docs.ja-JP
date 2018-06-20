---
title: PidTagCorrelate の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ce8573310e17e26b4e2deb4c0a0f835a6569151e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802661"
---
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="1b35d-103">PidTagCorrelate の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="1b35d-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="1b35d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b35d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b35d-105">メッセージの送信者のメッセージング システムの相互関係の機能を要求する場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="1b35d-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b35d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="1b35d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b35d-107">PR_CORRELATE</span><span class="sxs-lookup"><span data-stu-id="1b35d-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="1b35d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1b35d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b35d-109">0x0E0C</span><span class="sxs-lookup"><span data-stu-id="1b35d-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="1b35d-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="1b35d-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b35d-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1b35d-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1b35d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1b35d-112">Area:</span></span>  <br/> |<span data-ttu-id="1b35d-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="1b35d-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b35d-114">備考</span><span class="sxs-lookup"><span data-stu-id="1b35d-114">Remarks</span></span>

<span data-ttu-id="1b35d-115">元の送信メッセージと受信したレポートの相関関係を要求するこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="1b35d-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="1b35d-116">トランスポート プロバイダーでは、true を指定する**PR_CORRELATE**のセットを使用して発信されたメッセージが検出されると、そのメッセージのメッセージ転送システム (MTS) 識別子を**PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="1b35d-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="1b35d-117">X.400 など、MTS の id では、メッセージの相関関係をサポートしているシステムで**PR_CORRELATE**を使用してください。</span><span class="sxs-lookup"><span data-stu-id="1b35d-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1b35d-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1b35d-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1b35d-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1b35d-119">Header files</span></span>

<span data-ttu-id="1b35d-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b35d-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b35d-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1b35d-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b35d-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1b35d-122">Mapitags.h</span></span>
  
> <span data-ttu-id="1b35d-123">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1b35d-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b35d-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b35d-124">See also</span></span>



[<span data-ttu-id="1b35d-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1b35d-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b35d-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1b35d-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b35d-127">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="1b35d-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b35d-128">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="1b35d-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

