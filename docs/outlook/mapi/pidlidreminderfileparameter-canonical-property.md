---
title: PidLidReminderFileParameter の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1cfb8f7070a8001e94fa70e90c52635c9b8be122
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802122"
---
# <a name="pidlidreminderfileparameter-canonical-property"></a><span data-ttu-id="80f73-103">PidLidReminderFileParameter の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="80f73-103">PidLidReminderFileParameter Canonical Property</span></span>

  
  
<span data-ttu-id="80f73-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="80f73-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="80f73-105">クライアントがそのオブジェクトのアラームが期限切れになったときに再生されるサウンドのファイル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="80f73-105">Specifies the filename of the sound that a client should play when the reminder for that object becomes overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80f73-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="80f73-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80f73-107">dispidReminderFileParam</span><span class="sxs-lookup"><span data-stu-id="80f73-107">dispidReminderFileParam</span></span>  <br/> |
|<span data-ttu-id="80f73-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="80f73-108">Property set:</span></span>  <br/> |<span data-ttu-id="80f73-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="80f73-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="80f73-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="80f73-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="80f73-111">0x0000851F</span><span class="sxs-lookup"><span data-stu-id="80f73-111">0x0000851F</span></span>  <br/> |
|<span data-ttu-id="80f73-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="80f73-112">Data type:</span></span>  <br/> |<span data-ttu-id="80f73-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="80f73-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="80f73-114">領域:</span><span class="sxs-lookup"><span data-stu-id="80f73-114">Area:</span></span>  <br/> |<span data-ttu-id="80f73-115">アラーム</span><span class="sxs-lookup"><span data-stu-id="80f73-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80f73-116">備考</span><span class="sxs-lookup"><span data-stu-id="80f73-116">Remarks</span></span>

<span data-ttu-id="80f73-117">このプロパティが存在しない場合は、クライアントは、既定値を使用可能性があります。</span><span class="sxs-lookup"><span data-stu-id="80f73-117">If this property is not present, the client may use a default value.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="80f73-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="80f73-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80f73-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="80f73-119">Protocol specifications</span></span>

<span data-ttu-id="80f73-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80f73-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80f73-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="80f73-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="80f73-122">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80f73-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80f73-123">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="80f73-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80f73-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="80f73-124">Header files</span></span>

<span data-ttu-id="80f73-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80f73-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="80f73-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="80f73-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80f73-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="80f73-127">See also</span></span>



[<span data-ttu-id="80f73-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="80f73-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80f73-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="80f73-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80f73-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="80f73-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80f73-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="80f73-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

