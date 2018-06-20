---
title: PidLidReminderSet の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fd40be7733934002b81482a8bf5cfe8c9ce12313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802135"
---
# <a name="pidlidreminderset-canonical-property"></a><span data-ttu-id="5d5e3-103">PidLidReminderSet の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="5d5e3-103">PidLidReminderSet Canonical Property</span></span>

  
  
<span data-ttu-id="5d5e3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d5e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d5e3-105">オブジェクトにアラームを設定するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d5e3-105">Specifies whether a reminder is set on the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d5e3-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="5d5e3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d5e3-107">dispidReminderSet</span><span class="sxs-lookup"><span data-stu-id="5d5e3-107">dispidReminderSet</span></span>  <br/> |
|<span data-ttu-id="5d5e3-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5d5e3-108">Property set:</span></span>  <br/> |<span data-ttu-id="5d5e3-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5d5e3-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5d5e3-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5d5e3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5d5e3-111">0x00008503</span><span class="sxs-lookup"><span data-stu-id="5d5e3-111">0x00008503</span></span>  <br/> |
|<span data-ttu-id="5d5e3-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="5d5e3-112">Data type:</span></span>  <br/> |<span data-ttu-id="5d5e3-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5d5e3-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5d5e3-114">領域:</span><span class="sxs-lookup"><span data-stu-id="5d5e3-114">Area:</span></span>  <br/> |<span data-ttu-id="5d5e3-115">アラーム</span><span class="sxs-lookup"><span data-stu-id="5d5e3-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d5e3-116">備考</span><span class="sxs-lookup"><span data-stu-id="5d5e3-116">Remarks</span></span>

<span data-ttu-id="5d5e3-117">定期的な予定表オブジェクトにこのプロパティを TRUE に設定がある場合、クライアントは例外の値をオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="5d5e3-117">If a recurring calendar object has this property set to TRUE, the client can override this value for exceptions.</span></span>
  
<span data-ttu-id="5d5e3-118">このプロパティが FALSE の場合の例外を含め、シリーズ全体での定期的な予定表オブジェクトでアラームが無効になります。</span><span class="sxs-lookup"><span data-stu-id="5d5e3-118">If this property is FALSE on a recurring calendar object, reminders are disabled for the entire series, including exceptions.</span></span> <span data-ttu-id="5d5e3-119">定期的なタスクは、オブジェクトの例外が (詳細については、 [[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)と[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)を参照) でこのプロパティをオーバーライドできません。</span><span class="sxs-lookup"><span data-stu-id="5d5e3-119">For recurring task objects, this property cannot be overridden by exceptions (see [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) and [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) for details).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5d5e3-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5d5e3-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d5e3-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5d5e3-121">Protocol specifications</span></span>

<span data-ttu-id="5d5e3-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d5e3-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d5e3-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5d5e3-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5d5e3-124">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d5e3-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d5e3-125">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d5e3-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d5e3-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5d5e3-126">Header files</span></span>

<span data-ttu-id="5d5e3-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d5e3-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d5e3-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5d5e3-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d5e3-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d5e3-129">See also</span></span>



[<span data-ttu-id="5d5e3-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5d5e3-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d5e3-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5d5e3-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d5e3-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="5d5e3-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d5e3-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="5d5e3-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

