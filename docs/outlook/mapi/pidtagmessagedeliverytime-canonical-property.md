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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8ebaea7fb6888e51ee1ef658db53dcf3050644da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325614"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="c13fb-103">PidTagMessageDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c13fb-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="c13fb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c13fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c13fb-105">メッセージが配信された日時を格納します。</span><span class="sxs-lookup"><span data-stu-id="c13fb-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c13fb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c13fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c13fb-107">PR_MESSAGE_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="c13fb-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="c13fb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c13fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c13fb-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="c13fb-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="c13fb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c13fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="c13fb-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c13fb-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c13fb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c13fb-112">Area:</span></span>  <br/> |<span data-ttu-id="c13fb-113">メッセージ時刻</span><span class="sxs-lookup"><span data-stu-id="c13fb-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c13fb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c13fb-114">Remarks</span></span>

<span data-ttu-id="c13fb-115">このプロパティは、トランスポート プロバイダーがサーバーからローカル ストアにメッセージをコピーしたダウンロード時間ではなく、メッセージがサーバーに保存された時刻を表します。</span><span class="sxs-lookup"><span data-stu-id="c13fb-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c13fb-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c13fb-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c13fb-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c13fb-117">Protocol specifications</span></span>

<span data-ttu-id="c13fb-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c13fb-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c13fb-119">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c13fb-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c13fb-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c13fb-120">Header files</span></span>

<span data-ttu-id="c13fb-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c13fb-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="c13fb-122">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c13fb-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="c13fb-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c13fb-123">Mapitags.h</span></span>
  
> <span data-ttu-id="c13fb-124">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c13fb-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c13fb-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="c13fb-125">See also</span></span>



[<span data-ttu-id="c13fb-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c13fb-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c13fb-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c13fb-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c13fb-128">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c13fb-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c13fb-129">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c13fb-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

