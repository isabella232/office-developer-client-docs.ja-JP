---
title: PidTagMessageDeliveryTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDeliveryTime
api_type:
- HeaderDef
ms.assetid: 4f9d44f2-4faa-4f16-9e33-22f80c17db85
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4fd74e99a8073db03ad47292677ff98efca58af3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802975"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="ba144-103">PidTagMessageDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ba144-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="ba144-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ba144-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ba144-105">メッセージが配信されたときの日時が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ba144-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba144-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ba144-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ba144-107">PR_MESSAGE_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="ba144-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="ba144-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ba144-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ba144-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="ba144-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="ba144-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ba144-110">Data type:</span></span>  <br/> |<span data-ttu-id="ba144-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ba144-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ba144-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ba144-112">Area:</span></span>  <br/> |<span data-ttu-id="ba144-113">メッセージの時刻</span><span class="sxs-lookup"><span data-stu-id="ba144-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba144-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ba144-114">Remarks</span></span>

<span data-ttu-id="ba144-115">このプロパティは、ダウンロードにかかる時間とトランスポート プロバイダーは、メッセージ サーバーからコピーをローカル ストアではなく、メッセージがサーバーに格納されていた時間について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba144-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ba144-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ba144-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ba144-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ba144-117">Protocol specifications</span></span>

<span data-ttu-id="ba144-118">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba144-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba144-119">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ba144-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ba144-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ba144-120">Header files</span></span>

<span data-ttu-id="ba144-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ba144-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="ba144-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ba144-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="ba144-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ba144-123">Mapitags.h</span></span>
  
> <span data-ttu-id="ba144-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ba144-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ba144-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="ba144-125">See also</span></span>



[<span data-ttu-id="ba144-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ba144-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ba144-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ba144-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ba144-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ba144-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ba144-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ba144-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

