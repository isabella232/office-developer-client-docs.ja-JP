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
ms.openlocfilehash: c1a725583faf13fe8b46616d9d341798298a8b53
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563437"
---
# <a name="pidlidremindersignaltime-canonical-property"></a><span data-ttu-id="abd5c-103">PidLidReminderSignalTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="abd5c-103">PidLidReminderSignalTime Canonical Property</span></span>

  
  
<span data-ttu-id="abd5c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abd5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abd5c-105">アラームから遷移する保留中の期限切れのポイントを指定します。</span><span class="sxs-lookup"><span data-stu-id="abd5c-105">Specifies the point in time when a reminder transitions from pending to overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="abd5c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="abd5c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="abd5c-107">dispidReminderNextTime</span><span class="sxs-lookup"><span data-stu-id="abd5c-107">dispidReminderNextTime</span></span>  <br/> |
|<span data-ttu-id="abd5c-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="abd5c-108">Property set:</span></span>  <br/> |<span data-ttu-id="abd5c-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="abd5c-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="abd5c-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="abd5c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="abd5c-111">0x00008560</span><span class="sxs-lookup"><span data-stu-id="abd5c-111">0x00008560</span></span>  <br/> |
|<span data-ttu-id="abd5c-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="abd5c-112">Data type:</span></span>  <br/> |<span data-ttu-id="abd5c-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="abd5c-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="abd5c-114">領域:</span><span class="sxs-lookup"><span data-stu-id="abd5c-114">Area:</span></span>  <br/> |<span data-ttu-id="abd5c-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="abd5c-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abd5c-116">注釈</span><span class="sxs-lookup"><span data-stu-id="abd5c-116">Remarks</span></span>

<span data-ttu-id="abd5c-117">**DispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) プロパティが TRUE の場合、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="abd5c-117">This property must be set if the **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="abd5c-118">クライアントは、世界協定時刻 (UTC) で値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="abd5c-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="abd5c-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="abd5c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="abd5c-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="abd5c-120">Protocol specifications</span></span>

<span data-ttu-id="abd5c-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abd5c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abd5c-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="abd5c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="abd5c-123">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abd5c-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abd5c-124">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="abd5c-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="abd5c-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="abd5c-125">Header files</span></span>

<span data-ttu-id="abd5c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="abd5c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="abd5c-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="abd5c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abd5c-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="abd5c-128">See also</span></span>



[<span data-ttu-id="abd5c-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="abd5c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="abd5c-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="abd5c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="abd5c-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="abd5c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="abd5c-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="abd5c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

