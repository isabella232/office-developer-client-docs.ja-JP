---
title: PidLidClipStart 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidClipStart
api_type:
- COM
ms.assetid: d348988d-a84e-4318-8d48-62e4982ebaf1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a2bbaaee9325a7d2c110ff4082e14a249e4dc16
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577703"
---
# <a name="pidlidclipstart-canonical-property"></a><span data-ttu-id="468e7-103">PidLidClipStart 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="468e7-103">PidLidClipStart Canonical Property</span></span>

  
  
<span data-ttu-id="468e7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="468e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="468e7-105">カレンダー オブジェクトのインスタンスを 1 つの世界協定世界協定時刻 (UTC) でイベントの開始日時が指定し、定期的な一連の最初のインスタンスでは、UTC の日付の午前 0 時を指定します。</span><span class="sxs-lookup"><span data-stu-id="468e7-105">Specifies the start date and time of the event in Coordinated Universal Times (UTC) for single instance calendar objects, and specifies midnight on the date of the first instance in UTC for a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="468e7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="468e7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="468e7-107">dispidClipStart</span><span class="sxs-lookup"><span data-stu-id="468e7-107">dispidClipStart</span></span>  <br/> |
|<span data-ttu-id="468e7-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="468e7-108">Property set:</span></span>  <br/> |<span data-ttu-id="468e7-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="468e7-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="468e7-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="468e7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="468e7-111">0x00008235</span><span class="sxs-lookup"><span data-stu-id="468e7-111">0x00008235</span></span>  <br/> |
|<span data-ttu-id="468e7-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="468e7-112">Data type:</span></span>  <br/> |<span data-ttu-id="468e7-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="468e7-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="468e7-114">領域:</span><span class="sxs-lookup"><span data-stu-id="468e7-114">Area:</span></span>  <br/> |<span data-ttu-id="468e7-115">予定表</span><span class="sxs-lookup"><span data-stu-id="468e7-115">Calendar</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="468e7-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="468e7-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="468e7-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="468e7-117">Protocol specifications</span></span>

<span data-ttu-id="468e7-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="468e7-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="468e7-119">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="468e7-119">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="468e7-120">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="468e7-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="468e7-121">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="468e7-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="468e7-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="468e7-122">Header files</span></span>

<span data-ttu-id="468e7-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="468e7-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="468e7-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="468e7-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="468e7-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="468e7-125">See also</span></span>



[<span data-ttu-id="468e7-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="468e7-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="468e7-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="468e7-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="468e7-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="468e7-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="468e7-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="468e7-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

