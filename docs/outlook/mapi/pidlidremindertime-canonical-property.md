---
title: PidLidReminderTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderTime
api_type:
- COM
ms.assetid: f4068ff0-2aa2-4332-be7d-ecebda30dfff
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8371418aabc557f48c74039320305df59624d7ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358710"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="45ee5-103">PidLidReminderTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="45ee5-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="45ee5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45ee5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45ee5-105">アラームの初期シグナル時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="45ee5-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45ee5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="45ee5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45ee5-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="45ee5-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="45ee5-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="45ee5-108">Property set:</span></span>  <br/> |<span data-ttu-id="45ee5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="45ee5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="45ee5-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="45ee5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="45ee5-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="45ee5-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="45ee5-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="45ee5-112">Data type:</span></span>  <br/> |<span data-ttu-id="45ee5-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="45ee5-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="45ee5-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="45ee5-114">Area:</span></span>  <br/> |<span data-ttu-id="45ee5-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="45ee5-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45ee5-116">解説</span><span class="sxs-lookup"><span data-stu-id="45ee5-116">Remarks</span></span>

<span data-ttu-id="45ee5-117">calendar オブジェクトの場合、このプロパティは、予定の開始時刻であるユーザーの遅延時間を表します。</span><span class="sxs-lookup"><span data-stu-id="45ee5-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="45ee5-118">クライアントは協定世界時 (UTC) で値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45ee5-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45ee5-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="45ee5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45ee5-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="45ee5-120">Protocol specifications</span></span>

<span data-ttu-id="45ee5-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45ee5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45ee5-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="45ee5-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45ee5-123">[[OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45ee5-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45ee5-124">電子メールおよびその他のオブジェクトの事前通知のプロパティと相互作用モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="45ee5-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45ee5-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="45ee5-125">Header files</span></span>

<span data-ttu-id="45ee5-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45ee5-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="45ee5-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="45ee5-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45ee5-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="45ee5-128">See also</span></span>



[<span data-ttu-id="45ee5-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="45ee5-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45ee5-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="45ee5-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45ee5-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="45ee5-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45ee5-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="45ee5-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

