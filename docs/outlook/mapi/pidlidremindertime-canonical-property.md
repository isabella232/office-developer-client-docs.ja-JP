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
ms.openlocfilehash: dd1daddbdf4e953dac53d44181fedf371ce3beb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573881"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="0ed97-103">PidLidReminderTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0ed97-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="0ed97-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ed97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ed97-105">アラームの初期のシグナルの時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="0ed97-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ed97-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0ed97-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ed97-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="0ed97-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="0ed97-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0ed97-108">Property set:</span></span>  <br/> |<span data-ttu-id="0ed97-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="0ed97-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="0ed97-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0ed97-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0ed97-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="0ed97-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="0ed97-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0ed97-112">Data type:</span></span>  <br/> |<span data-ttu-id="0ed97-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="0ed97-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="0ed97-114">領域:</span><span class="sxs-lookup"><span data-stu-id="0ed97-114">Area:</span></span>  <br/> |<span data-ttu-id="0ed97-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="0ed97-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ed97-116">注釈</span><span class="sxs-lookup"><span data-stu-id="0ed97-116">Remarks</span></span>

<span data-ttu-id="0ed97-117">カレンダー オブジェクトは、このプロパティは、予定の開始時刻である場合、あるユーザーは、遅延時間で表します。</span><span class="sxs-lookup"><span data-stu-id="0ed97-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="0ed97-118">クライアントは、世界協定時刻 (UTC) で値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ed97-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0ed97-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0ed97-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ed97-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0ed97-120">Protocol specifications</span></span>

<span data-ttu-id="0ed97-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ed97-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ed97-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0ed97-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ed97-123">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ed97-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ed97-124">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="0ed97-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ed97-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0ed97-125">Header files</span></span>

<span data-ttu-id="0ed97-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ed97-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ed97-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0ed97-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ed97-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="0ed97-128">See also</span></span>



[<span data-ttu-id="0ed97-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0ed97-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ed97-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0ed97-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ed97-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0ed97-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ed97-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0ed97-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

