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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d6374c2fd3c277e2bb976930e9e105cc839b1e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359879"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="d2e6a-103">PidTagDeferredSendTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d2e6a-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="d2e6a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2e6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2e6a-105">クライアントがメッセージの送信を延期する時刻を示します。</span><span class="sxs-lookup"><span data-stu-id="d2e6a-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2e6a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d2e6a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d2e6a-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="d2e6a-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="d2e6a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d2e6a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d2e6a-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="d2e6a-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="d2e6a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d2e6a-110">Data type:</span></span>  <br/> |<span data-ttu-id="d2e6a-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d2e6a-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d2e6a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d2e6a-112">Area:</span></span>  <br/> |<span data-ttu-id="d2e6a-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="d2e6a-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2e6a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d2e6a-114">Remarks</span></span>

<span data-ttu-id="d2e6a-115">**PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) プロパティと **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) プロパティが存在する場合、このプロパティの値は次の数式を使用して再計算され、古い値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="d2e6a-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="d2e6a-116">**PR_DEFERRED_SEND_TIME**  = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) **+** PR_DEFERRED_SEND_NUMBER \* TimeOf(PR_DEFERRED_SEND_UNITS )</span><span class="sxs-lookup"><span data-stu-id="d2e6a-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="d2e6a-117">値 **PR_DEFERRED_SEND_TIME** 現在の時刻 (UTC) より前の場合、メッセージはすぐに送信されます。</span><span class="sxs-lookup"><span data-stu-id="d2e6a-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d2e6a-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d2e6a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d2e6a-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d2e6a-119">Protocol specifications</span></span>

<span data-ttu-id="d2e6a-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2e6a-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2e6a-121">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d2e6a-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d2e6a-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d2e6a-122">Header files</span></span>

<span data-ttu-id="d2e6a-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2e6a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d2e6a-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d2e6a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d2e6a-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d2e6a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d2e6a-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d2e6a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2e6a-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2e6a-127">See also</span></span>



[<span data-ttu-id="d2e6a-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d2e6a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d2e6a-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d2e6a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d2e6a-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d2e6a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d2e6a-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d2e6a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

