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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: efd0dcc8fc01fa433cbbf30936244e4818f8b14a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803584"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="9d6ec-103">PidTagStatusCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d6ec-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="9d6ec-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d6ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d6ec-105">セッション リソースの現在の状態を示すフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="9d6ec-106">すべてのサービス プロバイダーは、MAPI サブシステム、MAPI スプーラーを無効、および統合されたアドレス帳のステータスを報告するように、ステータス コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d6ec-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9d6ec-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d6ec-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="9d6ec-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="9d6ec-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="9d6ec-109">Identifier:</span></span>  <br/> |<span data-ttu-id="9d6ec-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="9d6ec-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="9d6ec-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9d6ec-111">Data type:</span></span>  <br/> |<span data-ttu-id="9d6ec-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9d6ec-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9d6ec-113">領域:</span><span class="sxs-lookup"><span data-stu-id="9d6ec-113">Area:</span></span>  <br/> |<span data-ttu-id="9d6ec-114">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="9d6ec-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d6ec-115">注釈</span><span class="sxs-lookup"><span data-stu-id="9d6ec-115">Remarks</span></span>

<span data-ttu-id="9d6ec-116">ステータス コードは必要があります、すべてのプロバイダー、Mapisvc.inf ファイルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="9d6ec-117">状態オブジェクトは、MAPI とすべてのサービス プロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="9d6ec-118">ステータス コード、ステータスのすべてのオブジェクトのセットを 1 つだけのトランスポート プロバイダーの別のセットの有効な値の 2 つのセットがあります。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="9d6ec-119">ステータスのすべてのオブジェクトは、次の値にこのプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="9d6ec-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="9d6ec-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="9d6ec-121">リソースを運用することを示します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="9d6ec-122">STATUS_FAILURE</span><span class="sxs-lookup"><span data-stu-id="9d6ec-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="9d6ec-123">リソースに問題が発生していることを示します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="9d6ec-124">STATUS_FAILURE では、サービス プロバイダーは、プロバイダー可能性がありますすぐに、シャット ダウンしている現在のセッションを終了することを示します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="9d6ec-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="9d6ec-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="9d6ec-126">ローカルのデータやサービスが利用できることを示します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="9d6ec-127">トランスポート プロバイダー プロパティも設定できます、状態オブジェクトの**PR_STATUS_CODE**に次の値。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="9d6ec-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="9d6ec-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="9d6ec-129">トランスポート プロバイダーが、受信メッセージを受信していることを示します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="9d6ec-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="9d6ec-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="9d6ec-131">トランスポート プロバイダーは、受信メッセージを受信できることを示します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="9d6ec-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="9d6ec-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="9d6ec-133">トランスポート プロバイダーが受信キューからメッセージをダウンロードしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="9d6ec-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="9d6ec-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="9d6ec-135">トランスポート プロバイダーが送信メッセージを受信していることを示します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="9d6ec-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="9d6ec-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="9d6ec-137">トランスポート プロバイダーが送信メッセージを処理できることを示します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="9d6ec-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="9d6ec-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="9d6ec-139">トランスポート プロバイダーが送信キューからメッセージをアップロードすることを示します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="9d6ec-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9d6ec-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="9d6ec-141">トランスポート プロバイダーがリモート アクセスをサポートしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="9d6ec-142">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9d6ec-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9d6ec-143">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9d6ec-143">Header files</span></span>

<span data-ttu-id="9d6ec-144">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d6ec-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d6ec-145">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d6ec-146">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9d6ec-146">Mapitags.h</span></span>
  
> <span data-ttu-id="9d6ec-147">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d6ec-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d6ec-148">See also</span></span>



[<span data-ttu-id="9d6ec-149">PidTagStatusString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d6ec-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="9d6ec-150">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d6ec-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d6ec-151">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d6ec-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d6ec-152">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9d6ec-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d6ec-153">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9d6ec-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

