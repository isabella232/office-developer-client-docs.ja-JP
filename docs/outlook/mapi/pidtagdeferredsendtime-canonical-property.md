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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359879"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="5f82f-103">PidTagDeferredSendTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f82f-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="5f82f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f82f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f82f-105">クライアントがメッセージの送信を延期しようとしている時間を示します。</span><span class="sxs-lookup"><span data-stu-id="5f82f-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f82f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5f82f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f82f-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="5f82f-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="5f82f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5f82f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5f82f-109">0x3fef</span><span class="sxs-lookup"><span data-stu-id="5f82f-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="5f82f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5f82f-110">Data type:</span></span>  <br/> |<span data-ttu-id="5f82f-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5f82f-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5f82f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5f82f-112">Area:</span></span>  <br/> |<span data-ttu-id="5f82f-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="5f82f-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f82f-114">解説</span><span class="sxs-lookup"><span data-stu-id="5f82f-114">Remarks</span></span>

<span data-ttu-id="5f82f-115">**PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) および**PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) プロパティが存在する場合、このプロパティの値は次の数式を使用して再計算されます。古い値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="5f82f-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="5f82f-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* timeof (**PR_DEFERRED_SEND_UNITS**)</span><span class="sxs-lookup"><span data-stu-id="5f82f-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="5f82f-117">**PR_DEFERRED_SEND_TIME** value が現在の時刻 (UTC) よりも早い場合、メッセージは直ちに送信されます。</span><span class="sxs-lookup"><span data-stu-id="5f82f-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5f82f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5f82f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f82f-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5f82f-119">Protocol specifications</span></span>

<span data-ttu-id="5f82f-120">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f82f-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f82f-121">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f82f-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f82f-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="5f82f-122">Header files</span></span>

<span data-ttu-id="5f82f-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f82f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f82f-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5f82f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f82f-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="5f82f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="5f82f-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5f82f-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f82f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f82f-127">See also</span></span>



[<span data-ttu-id="5f82f-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5f82f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f82f-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f82f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f82f-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5f82f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f82f-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5f82f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

