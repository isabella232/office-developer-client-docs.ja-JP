---
title: PidLidExceptionReplaceTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidExceptionReplaceTime
api_type:
- COM
ms.assetid: c3aae4f5-7f00-45bf-b007-370041ba360e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b364fb91bda7e895b546f9a281ef14ce33b073f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337983"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a><span data-ttu-id="7fc69-103">PidLidExceptionReplaceTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7fc69-103">PidLidExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="7fc69-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fc69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fc69-105">例外が置き換わる定期的なパターン内の日付と時刻を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fc69-105">Specifies the date and time within the recurrence pattern that the exception will replace.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7fc69-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7fc69-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7fc69-107">dispidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="7fc69-107">dispidExceptionReplaceTime</span></span>  <br/> |
|<span data-ttu-id="7fc69-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="7fc69-108">Property set:</span></span>  <br/> |<span data-ttu-id="7fc69-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="7fc69-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="7fc69-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7fc69-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7fc69-111">0x00008228</span><span class="sxs-lookup"><span data-stu-id="7fc69-111">0x00008228</span></span>  <br/> |
|<span data-ttu-id="7fc69-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7fc69-112">Data type:</span></span>  <br/> |<span data-ttu-id="7fc69-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7fc69-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7fc69-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="7fc69-114">Area:</span></span>  <br/> |<span data-ttu-id="7fc69-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="7fc69-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fc69-116">注釈</span><span class="sxs-lookup"><span data-stu-id="7fc69-116">Remarks</span></span>

<span data-ttu-id="7fc69-117">値は協定世界時 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fc69-117">The value must be specified in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="7fc69-118">このプロパティを使用すると、特定のインスタンスに対して例外添付ファイル オブジェクトを見つけます。</span><span class="sxs-lookup"><span data-stu-id="7fc69-118">This property allows the exception attachment object to be found for a particular instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7fc69-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7fc69-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7fc69-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7fc69-120">Protocol specifications</span></span>

<span data-ttu-id="7fc69-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fc69-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fc69-122">プロパティ セットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7fc69-122">Provides property set definitions.</span></span>
    
<span data-ttu-id="7fc69-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fc69-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fc69-124">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fc69-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7fc69-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7fc69-125">Header files</span></span>

<span data-ttu-id="7fc69-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7fc69-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7fc69-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7fc69-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7fc69-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="7fc69-128">See also</span></span>



[<span data-ttu-id="7fc69-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7fc69-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7fc69-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7fc69-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7fc69-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7fc69-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7fc69-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7fc69-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

