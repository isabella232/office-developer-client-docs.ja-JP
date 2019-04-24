---
title: PidTagDeferredDeliveryTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredDeliveryTime
api_type:
- HeaderDef
ms.assetid: 263ac923-692f-40d4-bdd5-116dc5c49766
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7197159fd55016454de3fa806fc30d0700ef5f3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359928"
---
# <a name="pidtagdeferreddeliverytime-canonical-property"></a><span data-ttu-id="8e2c6-103">PidTagDeferredDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e2c6-103">PidTagDeferredDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="8e2c6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e2c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e2c6-105">メッセージ送信者がメッセージを配信する日時が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8e2c6-105">Contains the date and time when a message sender wants a message delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e2c6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8e2c6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e2c6-107">PR_DEFERRED_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="8e2c6-107">PR_DEFERRED_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="8e2c6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8e2c6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e2c6-109">0x000f</span><span class="sxs-lookup"><span data-stu-id="8e2c6-109">0x000F</span></span>  <br/> |
|<span data-ttu-id="8e2c6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8e2c6-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e2c6-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="8e2c6-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="8e2c6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8e2c6-112">Area:</span></span>  <br/> |<span data-ttu-id="8e2c6-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="8e2c6-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e2c6-114">解説</span><span class="sxs-lookup"><span data-stu-id="8e2c6-114">Remarks</span></span>

<span data-ttu-id="8e2c6-115">MAPI では、遅延配信は実行されません。これは、遅延配信を処理するための基礎となるメッセージングシステムのオプションです。</span><span class="sxs-lookup"><span data-stu-id="8e2c6-115">MAPI does not perform the deferred delivery; it is an option of the underlying messaging system to handle deferred delivery.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8e2c6-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8e2c6-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e2c6-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8e2c6-117">Protocol specifications</span></span>

<span data-ttu-id="8e2c6-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e2c6-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e2c6-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e2c6-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e2c6-120">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e2c6-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e2c6-121">電子メールメッセージに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8e2c6-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e2c6-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="8e2c6-122">Header files</span></span>

<span data-ttu-id="8e2c6-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e2c6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e2c6-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e2c6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e2c6-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="8e2c6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="8e2c6-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8e2c6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e2c6-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e2c6-127">See also</span></span>



[<span data-ttu-id="8e2c6-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8e2c6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e2c6-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e2c6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e2c6-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8e2c6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e2c6-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8e2c6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

