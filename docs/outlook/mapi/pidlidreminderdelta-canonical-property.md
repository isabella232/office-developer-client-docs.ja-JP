---
title: PidLidReminderDelta の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e2caccf3cf6ca7e6f15bed1c901d4dfbb198f19b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802103"
---
# <a name="pidlidreminderdelta-canonical-property"></a><span data-ttu-id="3e300-103">PidLidReminderDelta の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="3e300-103">PidLidReminderDelta Canonical Property</span></span>

  
  
<span data-ttu-id="3e300-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3e300-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3e300-105">アラームが最初に期限切れの時刻と開始時刻、カレンダー オブジェクトの間隔を分単位で間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="3e300-105">Specifies the interval, in minutes, between the time when the reminder first becomes overdue and the start time of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3e300-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="3e300-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3e300-107">dispidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="3e300-107">dispidReminderDelta</span></span>  <br/> |
|<span data-ttu-id="3e300-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3e300-108">Property set:</span></span>  <br/> |<span data-ttu-id="3e300-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="3e300-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="3e300-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="3e300-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3e300-111">0x00008501</span><span class="sxs-lookup"><span data-stu-id="3e300-111">0x00008501</span></span>  <br/> |
|<span data-ttu-id="3e300-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="3e300-112">Data type:</span></span>  <br/> |<span data-ttu-id="3e300-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3e300-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3e300-114">領域:</span><span class="sxs-lookup"><span data-stu-id="3e300-114">Area:</span></span>  <br/> |<span data-ttu-id="3e300-115">アラーム</span><span class="sxs-lookup"><span data-stu-id="3e300-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e300-116">備考</span><span class="sxs-lookup"><span data-stu-id="3e300-116">Remarks</span></span>

<span data-ttu-id="3e300-117">カレンダー オブジェクトに対してこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e300-117">This property must be set on calendar objects.</span></span> <span data-ttu-id="3e300-118">以外のカレンダーのすべてのオブジェクトに対してこのプロパティが"0x00000000"に設定する必要がありますされ、無視されます。</span><span class="sxs-lookup"><span data-stu-id="3e300-118">For all non-calendar objects, this property should be set to "0x00000000" and is ignored.</span></span> <span data-ttu-id="3e300-119">定期的な予定表オブジェクトのインスタンスが 1 つのアラームが消去されたとき、このプロパティの値は次のインスタンスをシグナルの時間の計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e300-119">When a reminder is dismissed for one instance of a recurring calendar object, the value of this property is used in the calculation of the signal time for the next instance.</span></span> <span data-ttu-id="3e300-120">カレンダー オブジェクトの作成の詳細については、 [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e300-120">See [[MS- OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) for details about calendar object creation.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3e300-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3e300-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3e300-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3e300-122">Protocol specifications</span></span>

<span data-ttu-id="3e300-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e300-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e300-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3e300-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3e300-125">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e300-125">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e300-126">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="3e300-126">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3e300-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3e300-127">Header files</span></span>

<span data-ttu-id="3e300-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3e300-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="3e300-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3e300-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e300-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e300-130">See also</span></span>



[<span data-ttu-id="3e300-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e300-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3e300-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e300-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3e300-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="3e300-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3e300-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="3e300-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

