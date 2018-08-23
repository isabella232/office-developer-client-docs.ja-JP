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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c056b0e587de06f6c32ceb3cebbb96f2fb737208
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579082"
---
# <a name="pidlidreminderset-canonical-property"></a><span data-ttu-id="fc6b0-103">PidLidReminderSet 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fc6b0-103">PidLidReminderSet Canonical Property</span></span>

  
  
<span data-ttu-id="fc6b0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc6b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc6b0-105">オブジェクトにアラームを設定するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="fc6b0-105">Specifies whether a reminder is set on the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc6b0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fc6b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc6b0-107">dispidReminderSet</span><span class="sxs-lookup"><span data-stu-id="fc6b0-107">dispidReminderSet</span></span>  <br/> |
|<span data-ttu-id="fc6b0-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="fc6b0-108">Property set:</span></span>  <br/> |<span data-ttu-id="fc6b0-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fc6b0-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fc6b0-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fc6b0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fc6b0-111">0x00008503</span><span class="sxs-lookup"><span data-stu-id="fc6b0-111">0x00008503</span></span>  <br/> |
|<span data-ttu-id="fc6b0-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fc6b0-112">Data type:</span></span>  <br/> |<span data-ttu-id="fc6b0-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fc6b0-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fc6b0-114">領域:</span><span class="sxs-lookup"><span data-stu-id="fc6b0-114">Area:</span></span>  <br/> |<span data-ttu-id="fc6b0-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="fc6b0-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc6b0-116">注釈</span><span class="sxs-lookup"><span data-stu-id="fc6b0-116">Remarks</span></span>

<span data-ttu-id="fc6b0-117">定期的な予定表オブジェクトにこのプロパティを TRUE に設定がある場合、クライアントは例外の値をオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="fc6b0-117">If a recurring calendar object has this property set to TRUE, the client can override this value for exceptions.</span></span>
  
<span data-ttu-id="fc6b0-118">このプロパティが FALSE の場合の例外を含め、シリーズ全体での定期的な予定表オブジェクトでアラームが無効になります。</span><span class="sxs-lookup"><span data-stu-id="fc6b0-118">If this property is FALSE on a recurring calendar object, reminders are disabled for the entire series, including exceptions.</span></span> <span data-ttu-id="fc6b0-119">定期的なタスクは、オブジェクトの例外が (詳細については、 [[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)と[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)を参照) でこのプロパティをオーバーライドできません。</span><span class="sxs-lookup"><span data-stu-id="fc6b0-119">For recurring task objects, this property cannot be overridden by exceptions (see [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) and [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) for details).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fc6b0-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fc6b0-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc6b0-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fc6b0-121">Protocol specifications</span></span>

<span data-ttu-id="fc6b0-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc6b0-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc6b0-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fc6b0-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fc6b0-124">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc6b0-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc6b0-125">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="fc6b0-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc6b0-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fc6b0-126">Header files</span></span>

<span data-ttu-id="fc6b0-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc6b0-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc6b0-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fc6b0-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc6b0-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc6b0-129">See also</span></span>



[<span data-ttu-id="fc6b0-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fc6b0-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc6b0-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fc6b0-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc6b0-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fc6b0-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc6b0-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fc6b0-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

