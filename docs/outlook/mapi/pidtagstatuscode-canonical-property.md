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
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278758"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="36a87-103">PidTagStatusCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="36a87-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="36a87-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36a87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36a87-105">セッションリソースの現在の状態を示すフラグのビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="36a87-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="36a87-106">すべてのサービスプロバイダーは mapi として状態コードを設定し、サブシステム、mapi スプーラー、および統合アドレス帳の状態に関するレポートを作成します。</span><span class="sxs-lookup"><span data-stu-id="36a87-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36a87-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="36a87-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="36a87-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="36a87-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="36a87-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="36a87-109">Identifier:</span></span>  <br/> |<span data-ttu-id="36a87-110">0x3e04</span><span class="sxs-lookup"><span data-stu-id="36a87-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="36a87-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="36a87-111">Data type:</span></span>  <br/> |<span data-ttu-id="36a87-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="36a87-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="36a87-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="36a87-113">Area:</span></span>  <br/> |<span data-ttu-id="36a87-114">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="36a87-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36a87-115">解説</span><span class="sxs-lookup"><span data-stu-id="36a87-115">Remarks</span></span>

<span data-ttu-id="36a87-116">状態コードは、すべてのプロバイダーの mapisvc.inf ファイルに表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="36a87-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="36a87-117">状態オブジェクトは、MAPI およびすべてのサービスプロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="36a87-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="36a87-118">状態コードには2つの有効な値があり、すべての状態オブジェクトに1つ、トランスポートプロバイダーに対して別のセットが設定されています。</span><span class="sxs-lookup"><span data-stu-id="36a87-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="36a87-119">すべての status オブジェクトは、このプロパティを次の値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="36a87-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="36a87-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="36a87-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="36a87-121">リソースが稼働していることを示します。</span><span class="sxs-lookup"><span data-stu-id="36a87-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="36a87-122">STATUS_FAILURE</span><span class="sxs-lookup"><span data-stu-id="36a87-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="36a87-123">リソースに問題が発生していることを示します。</span><span class="sxs-lookup"><span data-stu-id="36a87-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="36a87-124">サービスプロバイダーの場合、STATUS_FAILURE は、プロバイダーがすぐにシャットダウンして現在のセッションを終了する可能性があることを示します。</span><span class="sxs-lookup"><span data-stu-id="36a87-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="36a87-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="36a87-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="36a87-126">ローカルデータまたはサービスのみが利用可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="36a87-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="36a87-127">また、トランスポートプロバイダーは、状態オブジェクトの**PR_STATUS_CODE**プロパティを次の値に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="36a87-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="36a87-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="36a87-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="36a87-129">トランスポートプロバイダーが受信メッセージを受信していることを示します。</span><span class="sxs-lookup"><span data-stu-id="36a87-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="36a87-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="36a87-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="36a87-131">トランスポートプロバイダーが受信メッセージを受信できることを示します。</span><span class="sxs-lookup"><span data-stu-id="36a87-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="36a87-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="36a87-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="36a87-133">トランスポートプロバイダーが受信キューからメッセージをダウンロードしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="36a87-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="36a87-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="36a87-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="36a87-135">トランスポートプロバイダーが送信メッセージを受信していることを示します。</span><span class="sxs-lookup"><span data-stu-id="36a87-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="36a87-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="36a87-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="36a87-137">トランスポートプロバイダーが送信メッセージを処理できることを示します。</span><span class="sxs-lookup"><span data-stu-id="36a87-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="36a87-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="36a87-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="36a87-139">トランスポートプロバイダーが送信キューからメッセージをアップロードしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="36a87-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="36a87-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="36a87-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="36a87-141">トランスポートプロバイダーがリモートアクセスをサポートしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="36a87-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="36a87-142">関連リソース</span><span class="sxs-lookup"><span data-stu-id="36a87-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="36a87-143">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="36a87-143">Header files</span></span>

<span data-ttu-id="36a87-144">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="36a87-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="36a87-145">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="36a87-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="36a87-146">Mapitags</span><span class="sxs-lookup"><span data-stu-id="36a87-146">Mapitags.h</span></span>
  
> <span data-ttu-id="36a87-147">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="36a87-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36a87-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="36a87-148">See also</span></span>



[<span data-ttu-id="36a87-149">PidTagStatusString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="36a87-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="36a87-150">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="36a87-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="36a87-151">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="36a87-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="36a87-152">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="36a87-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="36a87-153">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="36a87-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

