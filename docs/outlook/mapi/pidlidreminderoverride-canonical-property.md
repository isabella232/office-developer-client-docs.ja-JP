---
title: PidLidReminderOverride の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 59b1efdbb9757dbf75479eebfac8e7f67be5f587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802116"
---
# <a name="pidlidreminderoverride-canonical-property"></a><span data-ttu-id="f8803-103">PidLidReminderOverride の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f8803-103">PidLidReminderOverride Canonical Property</span></span>

  
  
<span data-ttu-id="f8803-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f8803-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f8803-105">クライアントが**dispidReminderPlaySound** ([PidLidReminderPlaySound](pidlidreminderplaysound-canonical-property.md)) と**dispidReminderFileParam** ( [PidLidReminderFileParameter ](pidlidreminderfileparameter-canonical-property.md)) のプロパティの値を遵守する必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f8803-105">Specifies whether the client should respect the values of the **dispidReminderPlaySound** ([PidLidReminderPlaySound](pidlidreminderplaysound-canonical-property.md)) and **dispidReminderFileParam** ( [ PidLidReminderFileParameter ](pidlidreminderfileparameter-canonical-property.md)) properties.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8803-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f8803-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8803-107">dispidReminderOverride</span><span class="sxs-lookup"><span data-stu-id="f8803-107">dispidReminderOverride</span></span>  <br/> |
|<span data-ttu-id="f8803-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f8803-108">Property set:</span></span>  <br/> |<span data-ttu-id="f8803-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f8803-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f8803-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f8803-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f8803-111">0x0000851C</span><span class="sxs-lookup"><span data-stu-id="f8803-111">0x0000851C</span></span>  <br/> |
|<span data-ttu-id="f8803-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8803-112">Data type:</span></span>  <br/> |<span data-ttu-id="f8803-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f8803-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f8803-114">領域:</span><span class="sxs-lookup"><span data-stu-id="f8803-114">Area:</span></span>  <br/> |<span data-ttu-id="f8803-115">アラーム</span><span class="sxs-lookup"><span data-stu-id="f8803-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8803-116">備考</span><span class="sxs-lookup"><span data-stu-id="f8803-116">Remarks</span></span>

<span data-ttu-id="f8803-117">クライアントは、 **dispidReminderPlaySound**および**dispidReminderFileParam**プロパティの値の代わりに既定値を使用可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f8803-117">A client may use default values in place of the values of the **dispidReminderPlaySound** and **dispidReminderFileParam** properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f8803-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f8803-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f8803-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f8803-119">Protocol specifications</span></span>

<span data-ttu-id="f8803-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8803-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8803-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f8803-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f8803-122">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8803-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8803-123">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="f8803-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f8803-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f8803-124">Header files</span></span>

<span data-ttu-id="f8803-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8803-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f8803-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f8803-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8803-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8803-127">See also</span></span>



[<span data-ttu-id="f8803-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f8803-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8803-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f8803-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8803-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="f8803-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8803-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="f8803-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

