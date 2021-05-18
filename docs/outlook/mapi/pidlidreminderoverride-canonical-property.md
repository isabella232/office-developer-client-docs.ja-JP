---
title: PidLidReminderOverride 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderOverride
api_type:
- COM
ms.assetid: ad7e37e1-bd12-409f-87e5-ebc0c298a072
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4956ce33d00135c34193dec3df832c6878b2c6db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360109"
---
# <a name="pidlidreminderoverride-canonical-property"></a><span data-ttu-id="25249-103">PidLidReminderOverride 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="25249-103">PidLidReminderOverride Canonical Property</span></span>

  
  
<span data-ttu-id="25249-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25249-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25249-105">クライアントが **dispidReminderPlaySound** [(PidLidReminderPlaySound)](pidlidreminderplaysound-canonical-property.md)および **dispidReminderFileParam** ( [ PidLidReminderFileParameter](pidlidreminderfileparameter-canonical-property.md)) プロパティの値を尊重するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="25249-105">Specifies whether the client should respect the values of the **dispidReminderPlaySound** ([PidLidReminderPlaySound](pidlidreminderplaysound-canonical-property.md)) and **dispidReminderFileParam** ( [ PidLidReminderFileParameter ](pidlidreminderfileparameter-canonical-property.md)) properties.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25249-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="25249-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25249-107">dispidReminderOverride</span><span class="sxs-lookup"><span data-stu-id="25249-107">dispidReminderOverride</span></span>  <br/> |
|<span data-ttu-id="25249-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="25249-108">Property set:</span></span>  <br/> |<span data-ttu-id="25249-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="25249-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="25249-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="25249-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="25249-111">0x0000851C</span><span class="sxs-lookup"><span data-stu-id="25249-111">0x0000851C</span></span>  <br/> |
|<span data-ttu-id="25249-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="25249-112">Data type:</span></span>  <br/> |<span data-ttu-id="25249-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="25249-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="25249-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="25249-114">Area:</span></span>  <br/> |<span data-ttu-id="25249-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="25249-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25249-116">注釈</span><span class="sxs-lookup"><span data-stu-id="25249-116">Remarks</span></span>

<span data-ttu-id="25249-117">クライアントは **、dispidReminderPlaySound** プロパティおよび **dispidReminderFileParam** プロパティの値に代わる既定値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="25249-117">A client may use default values in place of the values of the **dispidReminderPlaySound** and **dispidReminderFileParam** properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="25249-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="25249-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25249-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="25249-119">Protocol specifications</span></span>

<span data-ttu-id="25249-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25249-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25249-121">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="25249-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25249-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25249-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25249-123">メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="25249-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25249-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="25249-124">Header files</span></span>

<span data-ttu-id="25249-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25249-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="25249-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="25249-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25249-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="25249-127">See also</span></span>



[<span data-ttu-id="25249-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="25249-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25249-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="25249-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25249-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="25249-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25249-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="25249-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

