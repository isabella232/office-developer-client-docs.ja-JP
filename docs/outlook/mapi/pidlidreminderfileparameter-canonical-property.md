---
title: PidLidReminderFileParameter 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderFileParameter
api_type:
- COM
ms.assetid: 1009f0ea-6f35-484d-b04d-5b6e844c14dd
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 42eec18c74005e586657482ef6634669c489314d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360104"
---
# <a name="pidlidreminderfileparameter-canonical-property"></a><span data-ttu-id="c8bfb-103">PidLidReminderFileParameter 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c8bfb-103">PidLidReminderFileParameter Canonical Property</span></span>

  
  
<span data-ttu-id="c8bfb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8bfb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8bfb-105">そのオブジェクトのアラームが過剰になったときにクライアントが再生するサウンドのファイル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="c8bfb-105">Specifies the filename of the sound that a client should play when the reminder for that object becomes overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8bfb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c8bfb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8bfb-107">dispidReminderFileParam</span><span class="sxs-lookup"><span data-stu-id="c8bfb-107">dispidReminderFileParam</span></span>  <br/> |
|<span data-ttu-id="c8bfb-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="c8bfb-108">Property set:</span></span>  <br/> |<span data-ttu-id="c8bfb-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c8bfb-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c8bfb-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c8bfb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c8bfb-111">0x0000851F</span><span class="sxs-lookup"><span data-stu-id="c8bfb-111">0x0000851F</span></span>  <br/> |
|<span data-ttu-id="c8bfb-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c8bfb-112">Data type:</span></span>  <br/> |<span data-ttu-id="c8bfb-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c8bfb-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c8bfb-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="c8bfb-114">Area:</span></span>  <br/> |<span data-ttu-id="c8bfb-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="c8bfb-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8bfb-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c8bfb-116">Remarks</span></span>

<span data-ttu-id="c8bfb-117">このプロパティが存在しない場合、クライアントは既定値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c8bfb-117">If this property is not present, the client may use a default value.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c8bfb-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c8bfb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8bfb-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c8bfb-119">Protocol specifications</span></span>

<span data-ttu-id="c8bfb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8bfb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8bfb-121">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="c8bfb-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8bfb-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8bfb-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8bfb-123">メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="c8bfb-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8bfb-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c8bfb-124">Header files</span></span>

<span data-ttu-id="c8bfb-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8bfb-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8bfb-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c8bfb-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8bfb-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c8bfb-127">See also</span></span>



[<span data-ttu-id="c8bfb-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c8bfb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8bfb-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c8bfb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8bfb-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c8bfb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8bfb-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c8bfb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

