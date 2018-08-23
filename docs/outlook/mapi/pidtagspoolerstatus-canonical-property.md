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
ms.openlocfilehash: d04144a4f5ef714b59b608bfe19367bcb3c1ced8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588574"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="4dc63-103">PidTagSpoolerStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4dc63-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="4dc63-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4dc63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4dc63-105">MAPI スプーラーを無効に提供される情報に基づいて、メッセージのステータスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4dc63-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4dc63-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4dc63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4dc63-107">PR_SPOOLER_STATUS</span><span class="sxs-lookup"><span data-stu-id="4dc63-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="4dc63-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4dc63-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4dc63-109">0x0E10</span><span class="sxs-lookup"><span data-stu-id="4dc63-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="4dc63-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4dc63-110">Data type:</span></span>  <br/> |<span data-ttu-id="4dc63-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4dc63-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4dc63-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4dc63-112">Area:</span></span>  <br/> |<span data-ttu-id="4dc63-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="4dc63-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4dc63-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4dc63-114">Remarks</span></span>

<span data-ttu-id="4dc63-115">このプロパティは、メッセージ オブジェクトを MAPI によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="4dc63-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="4dc63-116">このプロパティは、受信したメッセージのみが表示され、他のすべてのケースで予約されています。</span><span class="sxs-lookup"><span data-stu-id="4dc63-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="4dc63-117">最終的な場所に、メッセージが配信されたかどうか、またはかどうかメッセージ フック プロバイダー可能性があるメッセージを削除して再ルーティング中にそのことを示します。</span><span class="sxs-lookup"><span data-stu-id="4dc63-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="4dc63-118">クライアント アプリケーションでは、このプロパティを設定する必要があることはありません。</span><span class="sxs-lookup"><span data-stu-id="4dc63-118">Client applications should never set this property.</span></span> <span data-ttu-id="4dc63-119">受信メッセージでは、クライアントまたはサービス プロバイダーは、メッセージの状態を確認するには、このプロパティに[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="4dc63-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="4dc63-120">値 S_OK は、メッセージがメッセージ ・ ストアに正常に配信されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="4dc63-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="4dc63-121">MAPI_E_OBJECT_DELETED の値は、メッセージは削除され、ストアにコミットされていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="4dc63-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="4dc63-122">メッセージ ストア プロバイダーは、メッセージ、受信者テーブル、および発信キューのテーブルでこのプロパティをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4dc63-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="4dc63-123">クライアントとプロバイダーが発信キュー テーブルに列を設定し、制限する必要がありますこのプロパティに基づいています。</span><span class="sxs-lookup"><span data-stu-id="4dc63-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4dc63-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4dc63-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4dc63-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4dc63-125">Header files</span></span>

<span data-ttu-id="4dc63-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4dc63-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4dc63-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4dc63-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4dc63-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4dc63-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4dc63-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4dc63-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4dc63-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="4dc63-130">See also</span></span>



[<span data-ttu-id="4dc63-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4dc63-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4dc63-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4dc63-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4dc63-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4dc63-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4dc63-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4dc63-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

