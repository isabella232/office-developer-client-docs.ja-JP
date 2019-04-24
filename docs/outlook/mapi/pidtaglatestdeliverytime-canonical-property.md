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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 77ca51ae5a0e7e1d5a9be8f4ca05a1187fe71694
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279853"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="f77ef-103">PidTagLatestDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f77ef-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="f77ef-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f77ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f77ef-105">メッセージ転送エージェント (MTA) がメッセージを配信する最新の日付と時刻が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f77ef-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f77ef-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f77ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f77ef-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="f77ef-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="f77ef-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f77ef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f77ef-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="f77ef-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="f77ef-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f77ef-110">Data type:</span></span>  <br/> |<span data-ttu-id="f77ef-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f77ef-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f77ef-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f77ef-112">Area:</span></span>  <br/> |<span data-ttu-id="f77ef-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="f77ef-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f77ef-114">解説</span><span class="sxs-lookup"><span data-stu-id="f77ef-114">Remarks</span></span>

<span data-ttu-id="f77ef-115">このプロパティが指定する時間に MTA がメッセージを配信できない場合は、配信なしでメッセージを取り消します。</span><span class="sxs-lookup"><span data-stu-id="f77ef-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f77ef-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f77ef-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f77ef-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="f77ef-117">Header files</span></span>

<span data-ttu-id="f77ef-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f77ef-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="f77ef-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f77ef-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="f77ef-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="f77ef-120">Mapitags.h</span></span>
  
> <span data-ttu-id="f77ef-121">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f77ef-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f77ef-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="f77ef-122">See also</span></span>



[<span data-ttu-id="f77ef-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f77ef-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f77ef-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f77ef-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f77ef-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f77ef-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f77ef-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f77ef-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

