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
ms.openlocfilehash: 07653bea747e6e697cb1edb5669ae106c9e213fe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591479"
---
# <a name="pidlidreminderfileparameter-canonical-property"></a><span data-ttu-id="49f58-103">PidLidReminderFileParameter 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="49f58-103">PidLidReminderFileParameter Canonical Property</span></span>

  
  
<span data-ttu-id="49f58-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49f58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49f58-105">クライアントがそのオブジェクトのアラームが期限切れになったときに再生されるサウンドのファイル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="49f58-105">Specifies the filename of the sound that a client should play when the reminder for that object becomes overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="49f58-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="49f58-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="49f58-107">dispidReminderFileParam</span><span class="sxs-lookup"><span data-stu-id="49f58-107">dispidReminderFileParam</span></span>  <br/> |
|<span data-ttu-id="49f58-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="49f58-108">Property set:</span></span>  <br/> |<span data-ttu-id="49f58-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="49f58-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="49f58-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="49f58-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="49f58-111">0x0000851F</span><span class="sxs-lookup"><span data-stu-id="49f58-111">0x0000851F</span></span>  <br/> |
|<span data-ttu-id="49f58-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="49f58-112">Data type:</span></span>  <br/> |<span data-ttu-id="49f58-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="49f58-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="49f58-114">領域:</span><span class="sxs-lookup"><span data-stu-id="49f58-114">Area:</span></span>  <br/> |<span data-ttu-id="49f58-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="49f58-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49f58-116">注釈</span><span class="sxs-lookup"><span data-stu-id="49f58-116">Remarks</span></span>

<span data-ttu-id="49f58-117">このプロパティが存在しない場合は、クライアントは、既定値を使用可能性があります。</span><span class="sxs-lookup"><span data-stu-id="49f58-117">If this property is not present, the client may use a default value.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="49f58-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="49f58-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="49f58-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="49f58-119">Protocol specifications</span></span>

<span data-ttu-id="49f58-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49f58-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49f58-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="49f58-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="49f58-122">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49f58-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49f58-123">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="49f58-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="49f58-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="49f58-124">Header files</span></span>

<span data-ttu-id="49f58-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49f58-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="49f58-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="49f58-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49f58-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="49f58-127">See also</span></span>



[<span data-ttu-id="49f58-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="49f58-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49f58-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="49f58-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49f58-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="49f58-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49f58-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="49f58-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

