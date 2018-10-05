---
title: PidTagDeferredSendTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendTime
api_type:
- HeaderDef
ms.assetid: ee206c2d-8371-4d19-b42b-78f6479e13ca
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d6374c2fd3c277e2bb976930e9e105cc839b1e8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397206"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="175c2-103">PidTagDeferredSendTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="175c2-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="175c2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="175c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="175c2-105">クライアントにはメッセージの送信を延期する時間を示します。</span><span class="sxs-lookup"><span data-stu-id="175c2-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="175c2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="175c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="175c2-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="175c2-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="175c2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="175c2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="175c2-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="175c2-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="175c2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="175c2-110">Data type:</span></span>  <br/> |<span data-ttu-id="175c2-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="175c2-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="175c2-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="175c2-112">Area:</span></span>  <br/> |<span data-ttu-id="175c2-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="175c2-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="175c2-114">備考</span><span class="sxs-lookup"><span data-stu-id="175c2-114">Remarks</span></span>

<span data-ttu-id="175c2-115">次の数式を使用して、このプロパティの値が再計算、 **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) と**PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) のプロパティが存在する場合、以前の値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="175c2-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="175c2-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* 水曜 (**PR_DEFERRED_SEND_UNITS**)</span><span class="sxs-lookup"><span data-stu-id="175c2-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="175c2-117">**PR_DEFERRED_SEND_TIME**の値が、現在の時刻 (UTC) より前の場合は、メッセージが直ちに送信されます。</span><span class="sxs-lookup"><span data-stu-id="175c2-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="175c2-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="175c2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="175c2-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="175c2-119">Protocol specifications</span></span>

<span data-ttu-id="175c2-120">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="175c2-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="175c2-121">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="175c2-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="175c2-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="175c2-122">Header files</span></span>

<span data-ttu-id="175c2-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="175c2-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="175c2-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="175c2-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="175c2-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="175c2-125">Mapitags.h</span></span>
  
> <span data-ttu-id="175c2-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="175c2-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="175c2-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="175c2-127">See also</span></span>



[<span data-ttu-id="175c2-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="175c2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="175c2-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="175c2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="175c2-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="175c2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="175c2-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="175c2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

