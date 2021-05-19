---
title: PidTagStatusCode 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418515"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="fe411-103">PidTagStatusCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fe411-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="fe411-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe411-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe411-105">セッション リソースの現在の状態を示すフラグのビットマスクが含まれる。</span><span class="sxs-lookup"><span data-stu-id="fe411-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="fe411-106">すべてのサービス プロバイダーは、MAPI と同じ状態コードを設定して、サブシステム、MAPI スプーラー、および統合アドレス帳の状態を報告します。</span><span class="sxs-lookup"><span data-stu-id="fe411-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe411-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fe411-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe411-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="fe411-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="fe411-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="fe411-109">Identifier:</span></span>  <br/> |<span data-ttu-id="fe411-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="fe411-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="fe411-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fe411-111">Data type:</span></span>  <br/> |<span data-ttu-id="fe411-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fe411-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fe411-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="fe411-113">Area:</span></span>  <br/> |<span data-ttu-id="fe411-114">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="fe411-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe411-115">注釈</span><span class="sxs-lookup"><span data-stu-id="fe411-115">Remarks</span></span>

<span data-ttu-id="fe411-116">状態コードは、すべてのプロバイダーの Mapisvc.inf ファイルに表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe411-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="fe411-117">Status オブジェクトは、MAPI およびすべてのサービス プロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="fe411-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="fe411-118">状態コードには 2 つの有効な値のセットがあります。1 つはすべての状態オブジェクトに対して設定され、もう 1 つはトランスポート プロバイダー専用のセットです。</span><span class="sxs-lookup"><span data-stu-id="fe411-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="fe411-119">すべての状態オブジェクトは、このプロパティを次の値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="fe411-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="fe411-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="fe411-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="fe411-121">リソースが運用可能な状態を示します。</span><span class="sxs-lookup"><span data-stu-id="fe411-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="fe411-122">STATUS_FAILURE</span><span class="sxs-lookup"><span data-stu-id="fe411-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="fe411-123">リソースに問題が発生している場合を示します。</span><span class="sxs-lookup"><span data-stu-id="fe411-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="fe411-124">サービス プロバイダーの場合、STATUS_FAILUREは、プロバイダーが現在のセッションを終了するためにすぐにシャットダウンされる可能性を示します。</span><span class="sxs-lookup"><span data-stu-id="fe411-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="fe411-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="fe411-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="fe411-126">ローカル データまたはサービスだけが使用可能な状態を示します。</span><span class="sxs-lookup"><span data-stu-id="fe411-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="fe411-127">トランスポート プロバイダーは、ステータス オブジェクトのプロパティPR_STATUS_CODE次 **の** 値に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="fe411-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="fe411-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="fe411-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="fe411-129">トランスポート プロバイダーが受信メッセージを受信中かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fe411-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="fe411-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="fe411-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="fe411-131">トランスポート プロバイダーが受信メッセージを受信できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fe411-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="fe411-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="fe411-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="fe411-133">トランスポート プロバイダーが受信キューからメッセージをダウンロード中かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fe411-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="fe411-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="fe411-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="fe411-135">トランスポート プロバイダーが送信メッセージを受信中かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fe411-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="fe411-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="fe411-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="fe411-137">トランスポート プロバイダーが送信メッセージを処理できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fe411-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="fe411-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="fe411-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="fe411-139">トランスポート プロバイダーが送信キューからメッセージをアップロード中かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fe411-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="fe411-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="fe411-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="fe411-141">トランスポート プロバイダーがリモート アクセスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fe411-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="fe411-142">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fe411-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fe411-143">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fe411-143">Header files</span></span>

<span data-ttu-id="fe411-144">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe411-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe411-145">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fe411-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="fe411-146">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fe411-146">Mapitags.h</span></span>
  
> <span data-ttu-id="fe411-147">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="fe411-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe411-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe411-148">See also</span></span>



[<span data-ttu-id="fe411-149">PidTagStatusString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fe411-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="fe411-150">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fe411-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe411-151">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fe411-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe411-152">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fe411-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe411-153">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fe411-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

