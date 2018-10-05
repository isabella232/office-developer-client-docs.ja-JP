---
title: PidLidReminderDelta 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderDelta
api_type:
- COM
ms.assetid: 011d73d0-8b38-4a4e-a56f-92dec451946a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 86a0203f930661452bb143e247c17ef6da8ed436
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398005"
---
# <a name="pidlidreminderdelta-canonical-property"></a><span data-ttu-id="026f0-103">PidLidReminderDelta 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="026f0-103">PidLidReminderDelta Canonical Property</span></span>

  
  
<span data-ttu-id="026f0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="026f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="026f0-105">アラームが最初に期限切れの時刻と開始時刻、カレンダー オブジェクトの間隔を分単位で間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="026f0-105">Specifies the interval, in minutes, between the time when the reminder first becomes overdue and the start time of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="026f0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="026f0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="026f0-107">dispidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="026f0-107">dispidReminderDelta</span></span>  <br/> |
|<span data-ttu-id="026f0-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="026f0-108">Property set:</span></span>  <br/> |<span data-ttu-id="026f0-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="026f0-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="026f0-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="026f0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="026f0-111">0x00008501</span><span class="sxs-lookup"><span data-stu-id="026f0-111">0x00008501</span></span>  <br/> |
|<span data-ttu-id="026f0-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="026f0-112">Data type:</span></span>  <br/> |<span data-ttu-id="026f0-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="026f0-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="026f0-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="026f0-114">Area:</span></span>  <br/> |<span data-ttu-id="026f0-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="026f0-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="026f0-116">備考</span><span class="sxs-lookup"><span data-stu-id="026f0-116">Remarks</span></span>

<span data-ttu-id="026f0-117">カレンダー オブジェクトに対してこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="026f0-117">This property must be set on calendar objects.</span></span> <span data-ttu-id="026f0-118">以外のカレンダーのすべてのオブジェクトに対してこのプロパティが"0x00000000"に設定する必要がありますされ、無視されます。</span><span class="sxs-lookup"><span data-stu-id="026f0-118">For all non-calendar objects, this property should be set to "0x00000000" and is ignored.</span></span> <span data-ttu-id="026f0-119">定期的な予定表オブジェクトのインスタンスが 1 つのアラームが消去されたとき、このプロパティの値は次のインスタンスをシグナルの時間の計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="026f0-119">When a reminder is dismissed for one instance of a recurring calendar object, the value of this property is used in the calculation of the signal time for the next instance.</span></span> <span data-ttu-id="026f0-120">カレンダー オブジェクトの作成の詳細については、 [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="026f0-120">See [[MS- OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) for details about calendar object creation.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="026f0-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="026f0-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="026f0-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="026f0-122">Protocol specifications</span></span>

<span data-ttu-id="026f0-123">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="026f0-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="026f0-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="026f0-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="026f0-125">[[MS OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="026f0-125">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="026f0-126">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="026f0-126">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="026f0-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="026f0-127">Header files</span></span>

<span data-ttu-id="026f0-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="026f0-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="026f0-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="026f0-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="026f0-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="026f0-130">See also</span></span>



[<span data-ttu-id="026f0-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="026f0-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="026f0-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="026f0-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="026f0-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="026f0-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="026f0-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="026f0-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

