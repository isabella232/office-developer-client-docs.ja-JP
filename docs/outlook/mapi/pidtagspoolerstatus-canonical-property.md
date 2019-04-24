---
title: PidTagSpoolerStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 426d26cae147faf3f843ac547de9d205d766ac44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348210"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="a6e43-103">PidTagSpoolerStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a6e43-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="a6e43-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6e43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6e43-105">MAPI スプーラーで使用可能な情報に基づいてメッセージの状態を格納します。</span><span class="sxs-lookup"><span data-stu-id="a6e43-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a6e43-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a6e43-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a6e43-107">PR_SPOOLER_STATUS</span><span class="sxs-lookup"><span data-stu-id="a6e43-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="a6e43-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a6e43-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a6e43-109">0x0e10</span><span class="sxs-lookup"><span data-stu-id="a6e43-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="a6e43-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a6e43-110">Data type:</span></span>  <br/> |<span data-ttu-id="a6e43-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a6e43-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a6e43-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a6e43-112">Area:</span></span>  <br/> |<span data-ttu-id="a6e43-113">MAPI ノンノンアウトテーブル</span><span class="sxs-lookup"><span data-stu-id="a6e43-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6e43-114">解説</span><span class="sxs-lookup"><span data-stu-id="a6e43-114">Remarks</span></span>

<span data-ttu-id="a6e43-115">このプロパティは、メッセージオブジェクトの MAPI によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="a6e43-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="a6e43-116">このプロパティは、受信メッセージのみに表示され、他のすべてのケースで予約されています。</span><span class="sxs-lookup"><span data-stu-id="a6e43-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="a6e43-117">メッセージが最終的な場所に配信されたかどうか、またはメッセージングフックプロバイダーがメッセージの再ルーティング中にメッセージを削除した可能性があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a6e43-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="a6e43-118">クライアントアプリケーションでこのプロパティを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="a6e43-118">Client applications should never set this property.</span></span> <span data-ttu-id="a6e43-119">受信メッセージの場合、クライアントまたはサービスプロバイダーは、このプロパティに[imapiprop:: GetProps](imapiprop-getprops.md)を呼び出して、メッセージの状態を確認できます。</span><span class="sxs-lookup"><span data-stu-id="a6e43-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="a6e43-120">値 S_OK は、メッセージがメッセージストアに正常に配信されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="a6e43-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="a6e43-121">値 MAPI_E_OBJECT_DELETED は、メッセージが削除され、ストアにコミットされていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="a6e43-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="a6e43-122">メッセージストアプロバイダーは、メッセージ、受信者テーブル、および送信キューテーブルでこのプロパティをサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6e43-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="a6e43-123">クライアントとプロバイダーは、送信キューテーブルの列を設定し、このプロパティに基づいて制限できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6e43-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a6e43-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a6e43-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a6e43-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a6e43-125">Header files</span></span>

<span data-ttu-id="a6e43-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a6e43-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a6e43-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a6e43-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a6e43-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="a6e43-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a6e43-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a6e43-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6e43-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6e43-130">See also</span></span>



[<span data-ttu-id="a6e43-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a6e43-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a6e43-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a6e43-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a6e43-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a6e43-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a6e43-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a6e43-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

