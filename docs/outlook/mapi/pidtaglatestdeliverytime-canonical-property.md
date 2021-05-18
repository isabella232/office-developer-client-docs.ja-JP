---
title: PidTagLatestDeliveryTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLatestDeliveryTime
api_type:
- HeaderDef
ms.assetid: 6c2e64bc-786e-4867-a504-46f4d1214337
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 77ca51ae5a0e7e1d5a9be8f4ca05a1187fe71694
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407789"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="d163a-103">PidTagLatestDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d163a-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="d163a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d163a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d163a-105">メッセージ転送エージェント (MTA) がメッセージを配信する必要がある最新の日時を含む。</span><span class="sxs-lookup"><span data-stu-id="d163a-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d163a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d163a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d163a-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="d163a-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="d163a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d163a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d163a-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="d163a-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="d163a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d163a-110">Data type:</span></span>  <br/> |<span data-ttu-id="d163a-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d163a-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d163a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d163a-112">Area:</span></span>  <br/> |<span data-ttu-id="d163a-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="d163a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d163a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d163a-114">Remarks</span></span>

<span data-ttu-id="d163a-115">MTA は、このプロパティが指定した時点でメッセージを配信できない場合、配信なしでメッセージをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="d163a-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d163a-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d163a-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d163a-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d163a-117">Header files</span></span>

<span data-ttu-id="d163a-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d163a-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="d163a-119">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d163a-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="d163a-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d163a-120">Mapitags.h</span></span>
  
> <span data-ttu-id="d163a-121">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d163a-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d163a-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="d163a-122">See also</span></span>



[<span data-ttu-id="d163a-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d163a-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d163a-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d163a-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d163a-125">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d163a-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d163a-126">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d163a-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

