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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 42eec18c74005e586657482ef6634669c489314d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360104"
---
# <a name="pidlidreminderfileparameter-canonical-property"></a><span data-ttu-id="32e78-103">PidLidReminderFileParameter 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="32e78-103">PidLidReminderFileParameter Canonical Property</span></span>

  
  
<span data-ttu-id="32e78-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32e78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32e78-105">そのオブジェクトのアラームが期限切れになったときにクライアントが再生するサウンドのファイル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="32e78-105">Specifies the filename of the sound that a client should play when the reminder for that object becomes overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="32e78-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="32e78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="32e78-107">dispidReminderFileParam</span><span class="sxs-lookup"><span data-stu-id="32e78-107">dispidReminderFileParam</span></span>  <br/> |
|<span data-ttu-id="32e78-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="32e78-108">Property set:</span></span>  <br/> |<span data-ttu-id="32e78-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="32e78-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="32e78-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="32e78-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="32e78-111">0x0000851f</span><span class="sxs-lookup"><span data-stu-id="32e78-111">0x0000851F</span></span>  <br/> |
|<span data-ttu-id="32e78-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="32e78-112">Data type:</span></span>  <br/> |<span data-ttu-id="32e78-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="32e78-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="32e78-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="32e78-114">Area:</span></span>  <br/> |<span data-ttu-id="32e78-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="32e78-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32e78-116">解説</span><span class="sxs-lookup"><span data-stu-id="32e78-116">Remarks</span></span>

<span data-ttu-id="32e78-117">このプロパティが存在しない場合、クライアントは既定値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="32e78-117">If this property is not present, the client may use a default value.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="32e78-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="32e78-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="32e78-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="32e78-119">Protocol specifications</span></span>

<span data-ttu-id="32e78-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32e78-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32e78-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="32e78-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="32e78-122">[[OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32e78-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32e78-123">電子メールおよびその他のオブジェクトの事前通知のプロパティと相互作用モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="32e78-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="32e78-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="32e78-124">Header files</span></span>

<span data-ttu-id="32e78-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="32e78-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="32e78-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="32e78-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="32e78-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="32e78-127">See also</span></span>



[<span data-ttu-id="32e78-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="32e78-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="32e78-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="32e78-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="32e78-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="32e78-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="32e78-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="32e78-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

