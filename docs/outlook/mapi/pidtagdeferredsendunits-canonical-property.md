---
title: PidTagDeferredSendUnits 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: becc076efe0f4f805eb2a8db071b70ad731ee256
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359907"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a><span data-ttu-id="2b52f-103">PidTagDeferredSendUnits 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2b52f-103">PidTagDeferredSendUnits Canonical Property</span></span>

  
  
<span data-ttu-id="2b52f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b52f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b52f-105">**PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) プロパティの値を乗算する時間の単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="2b52f-105">Specifies the unit of time by which the **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) property value should be multiplied.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2b52f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2b52f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b52f-107">PR_DEFERRED_SEND_UNITS</span><span class="sxs-lookup"><span data-stu-id="2b52f-107">PR_DEFERRED_SEND_UNITS</span></span>  <br/> |
|<span data-ttu-id="2b52f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2b52f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2b52f-109">0x3FEC</span><span class="sxs-lookup"><span data-stu-id="2b52f-109">0x3FEC</span></span>  <br/> |
|<span data-ttu-id="2b52f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2b52f-110">Data type:</span></span>  <br/> |<span data-ttu-id="2b52f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2b52f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2b52f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2b52f-112">Area:</span></span>  <br/> |<span data-ttu-id="2b52f-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="2b52f-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b52f-114">解説</span><span class="sxs-lookup"><span data-stu-id="2b52f-114">Remarks</span></span>

<span data-ttu-id="2b52f-115">設定されている場合、このプロパティには、次のいずれかの値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b52f-115">If set, this property must have one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2b52f-116">**PidTagDeferredSendUnits**</span><span class="sxs-lookup"><span data-stu-id="2b52f-116">**PidTagDeferredSendUnits**</span></span> <br/> |<span data-ttu-id="2b52f-117">説明</span><span class="sxs-lookup"><span data-stu-id="2b52f-117">Description</span></span>  <br/> |
|<span data-ttu-id="2b52f-118">.0</span><span class="sxs-lookup"><span data-stu-id="2b52f-118">0</span></span>  <br/> |<span data-ttu-id="2b52f-119">分 (60 秒など)</span><span class="sxs-lookup"><span data-stu-id="2b52f-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="2b52f-120">1-d</span><span class="sxs-lookup"><span data-stu-id="2b52f-120">1</span></span>  <br/> |<span data-ttu-id="2b52f-121">時間 (例: 60x60 秒)</span><span class="sxs-lookup"><span data-stu-id="2b52f-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="2b52f-122">pbm-2</span><span class="sxs-lookup"><span data-stu-id="2b52f-122">2</span></span>  <br/> |<span data-ttu-id="2b52f-123">日 (たとえば24x60x60 秒)</span><span class="sxs-lookup"><span data-stu-id="2b52f-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="2b52f-124">1/3</span><span class="sxs-lookup"><span data-stu-id="2b52f-124">3</span></span>  <br/> |<span data-ttu-id="2b52f-125">週 (7x24x60x60 秒など)</span><span class="sxs-lookup"><span data-stu-id="2b52f-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2b52f-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2b52f-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2b52f-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2b52f-127">Protocol specifications</span></span>

<span data-ttu-id="2b52f-128">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b52f-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b52f-129">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2b52f-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2b52f-130">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="2b52f-130">Header files</span></span>

<span data-ttu-id="2b52f-131">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b52f-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b52f-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2b52f-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="2b52f-133">Mapitags</span><span class="sxs-lookup"><span data-stu-id="2b52f-133">Mapitags.h</span></span>
  
> <span data-ttu-id="2b52f-134">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2b52f-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b52f-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b52f-135">See also</span></span>



[<span data-ttu-id="2b52f-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2b52f-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b52f-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2b52f-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b52f-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2b52f-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b52f-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2b52f-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

