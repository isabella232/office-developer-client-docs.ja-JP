---
title: PidLidReminderSet 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSet
api_type:
- COM
ms.assetid: 06b7792c-1b43-4e20-9a3b-44f2664b2125
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 59379b0b1345684a491f2f7f896f2b8fc8fd54c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335155"
---
# <a name="pidlidreminderset-canonical-property"></a><span data-ttu-id="328bf-103">PidLidReminderSet 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="328bf-103">PidLidReminderSet Canonical Property</span></span>

  
  
<span data-ttu-id="328bf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="328bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="328bf-105">オブジェクトにアラームを設定するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="328bf-105">Specifies whether a reminder is set on the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="328bf-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="328bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="328bf-107">dispidReminderSet</span><span class="sxs-lookup"><span data-stu-id="328bf-107">dispidReminderSet</span></span>  <br/> |
|<span data-ttu-id="328bf-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="328bf-108">Property set:</span></span>  <br/> |<span data-ttu-id="328bf-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="328bf-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="328bf-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="328bf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="328bf-111">0x00008503</span><span class="sxs-lookup"><span data-stu-id="328bf-111">0x00008503</span></span>  <br/> |
|<span data-ttu-id="328bf-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="328bf-112">Data type:</span></span>  <br/> |<span data-ttu-id="328bf-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="328bf-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="328bf-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="328bf-114">Area:</span></span>  <br/> |<span data-ttu-id="328bf-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="328bf-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="328bf-116">注釈</span><span class="sxs-lookup"><span data-stu-id="328bf-116">Remarks</span></span>

<span data-ttu-id="328bf-117">定期的な予定表オブジェクトにこのプロパティが TRUE に設定されている場合、クライアントは例外に対してこの値を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="328bf-117">If a recurring calendar object has this property set to TRUE, the client can override this value for exceptions.</span></span>
  
<span data-ttu-id="328bf-118">定期的な予定表オブジェクトでこのプロパティが FALSE の場合、例外を含む、系列全体に対してアラームが無効になります。</span><span class="sxs-lookup"><span data-stu-id="328bf-118">If this property is FALSE on a recurring calendar object, reminders are disabled for the entire series, including exceptions.</span></span> <span data-ttu-id="328bf-119">定期的なタスク オブジェクトの場合、このプロパティは例外によって上書きできません (詳細については [、「[MS-OXOCAL]」](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) および [「MS-OXOTASK」を](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) 参照)。</span><span class="sxs-lookup"><span data-stu-id="328bf-119">For recurring task objects, this property cannot be overridden by exceptions (see [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) and [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) for details).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="328bf-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="328bf-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="328bf-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="328bf-121">Protocol specifications</span></span>

<span data-ttu-id="328bf-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="328bf-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="328bf-123">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="328bf-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="328bf-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="328bf-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="328bf-125">メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="328bf-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="328bf-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="328bf-126">Header files</span></span>

<span data-ttu-id="328bf-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="328bf-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="328bf-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="328bf-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="328bf-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="328bf-129">See also</span></span>



[<span data-ttu-id="328bf-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="328bf-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="328bf-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="328bf-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="328bf-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="328bf-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="328bf-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="328bf-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

