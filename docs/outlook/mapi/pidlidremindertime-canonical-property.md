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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8371418aabc557f48c74039320305df59624d7ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358710"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="58f54-103">PidLidReminderTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="58f54-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="58f54-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58f54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58f54-105">アラームの初期信号時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="58f54-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58f54-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="58f54-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58f54-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="58f54-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="58f54-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="58f54-108">Property set:</span></span>  <br/> |<span data-ttu-id="58f54-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="58f54-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="58f54-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="58f54-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="58f54-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="58f54-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="58f54-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="58f54-112">Data type:</span></span>  <br/> |<span data-ttu-id="58f54-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="58f54-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="58f54-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="58f54-114">Area:</span></span>  <br/> |<span data-ttu-id="58f54-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="58f54-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58f54-116">注釈</span><span class="sxs-lookup"><span data-stu-id="58f54-116">Remarks</span></span>

<span data-ttu-id="58f54-117">予定表オブジェクトの場合、このプロパティは、予定の開始時刻であるユーザーが遅れた時刻を表します。</span><span class="sxs-lookup"><span data-stu-id="58f54-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="58f54-118">クライアントは、協定世界時 (UTC) で値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58f54-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="58f54-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="58f54-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58f54-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="58f54-120">Protocol specifications</span></span>

<span data-ttu-id="58f54-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58f54-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58f54-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="58f54-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58f54-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58f54-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58f54-124">メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="58f54-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58f54-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="58f54-125">Header files</span></span>

<span data-ttu-id="58f54-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58f54-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="58f54-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="58f54-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58f54-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="58f54-128">See also</span></span>



[<span data-ttu-id="58f54-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="58f54-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58f54-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="58f54-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58f54-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="58f54-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58f54-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="58f54-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

