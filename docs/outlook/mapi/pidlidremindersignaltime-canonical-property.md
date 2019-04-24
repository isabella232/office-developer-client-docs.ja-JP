---
title: PidLidReminderSignalTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSignalTime
api_type:
- COM
ms.assetid: 58f6432e-6e88-420b-959f-7f365899f7eb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3fcfd00f71a308dce625e6636edbe647f3d7258a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350856"
---
# <a name="pidlidremindersignaltime-canonical-property"></a><span data-ttu-id="ecb08-103">PidLidReminderSignalTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ecb08-103">PidLidReminderSignalTime Canonical Property</span></span>

  
  
<span data-ttu-id="ecb08-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecb08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecb08-105">アラームが保留中から期限切れに移行する時点を指定します。</span><span class="sxs-lookup"><span data-stu-id="ecb08-105">Specifies the point in time when a reminder transitions from pending to overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ecb08-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ecb08-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ecb08-107">dispidReminderNextTime</span><span class="sxs-lookup"><span data-stu-id="ecb08-107">dispidReminderNextTime</span></span>  <br/> |
|<span data-ttu-id="ecb08-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="ecb08-108">Property set:</span></span>  <br/> |<span data-ttu-id="ecb08-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ecb08-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ecb08-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ecb08-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ecb08-111">0x00008560</span><span class="sxs-lookup"><span data-stu-id="ecb08-111">0x00008560</span></span>  <br/> |
|<span data-ttu-id="ecb08-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ecb08-112">Data type:</span></span>  <br/> |<span data-ttu-id="ecb08-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ecb08-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ecb08-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="ecb08-114">Area:</span></span>  <br/> |<span data-ttu-id="ecb08-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="ecb08-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecb08-116">解説</span><span class="sxs-lookup"><span data-stu-id="ecb08-116">Remarks</span></span>

<span data-ttu-id="ecb08-117">**dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) プロパティが TRUE の場合は、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecb08-117">This property must be set if the **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="ecb08-118">クライアントは協定世界時 (UTC) で値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecb08-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ecb08-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ecb08-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ecb08-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ecb08-120">Protocol specifications</span></span>

<span data-ttu-id="ecb08-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecb08-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecb08-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ecb08-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ecb08-123">[[OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecb08-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecb08-124">電子メールおよびその他のオブジェクトの事前通知のプロパティと相互作用モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="ecb08-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ecb08-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="ecb08-125">Header files</span></span>

<span data-ttu-id="ecb08-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecb08-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ecb08-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ecb08-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecb08-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="ecb08-128">See also</span></span>



[<span data-ttu-id="ecb08-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ecb08-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ecb08-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ecb08-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ecb08-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ecb08-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ecb08-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ecb08-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

