---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350877"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="44f38-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="44f38-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="44f38-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44f38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44f38-105">MAPI クライアントがクライアントプロセスの高速シャットダウンを実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="44f38-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44f38-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="44f38-106">Header file:</span></span>  <br/> |<span data-ttu-id="44f38-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44f38-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="44f38-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="44f38-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="44f38-109">[imapisession](imapisessioniunknown.md)オブジェクト</span><span class="sxs-lookup"><span data-stu-id="44f38-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="44f38-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="44f38-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="44f38-111">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="44f38-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="44f38-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="44f38-112">Called by:</span></span>  <br/> |<span data-ttu-id="44f38-113">MAPI クライアント</span><span class="sxs-lookup"><span data-stu-id="44f38-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="44f38-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="44f38-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="44f38-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="44f38-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="44f38-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="44f38-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="44f38-117">lpmapiclientshutdown</span><span class="sxs-lookup"><span data-stu-id="44f38-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="44f38-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="44f38-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="44f38-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="44f38-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="44f38-120">読み込み済みの mapi プロバイダーによって提供される高速シャットダウンのサポートを mapi サブシステムに対して照会します。</span><span class="sxs-lookup"><span data-stu-id="44f38-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="44f38-121">notifyprocessshutdown</span><span class="sxs-lookup"><span data-stu-id="44f38-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="44f38-122">シャットダウンを続行する MAPI クライアントの意図を示します。</span><span class="sxs-lookup"><span data-stu-id="44f38-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="44f38-123">dofastshutdown</span><span class="sxs-lookup"><span data-stu-id="44f38-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="44f38-124">クライアントプロセスをすぐに終了する MAPI クライアントの意図を示します。</span><span class="sxs-lookup"><span data-stu-id="44f38-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44f38-125">解説</span><span class="sxs-lookup"><span data-stu-id="44f38-125">Remarks</span></span>

<span data-ttu-id="44f38-126">高速シャットダウンの目的は、mapi クライアントと、mapi の設定とデータを保存するために mapi クライアントがアクティブな mapi セッションを持つ、すべての読み込み済みの mapi プロバイダーを許可することです。</span><span class="sxs-lookup"><span data-stu-id="44f38-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="44f38-127">これにより、MAPI クライアントは、データ損失を発生させることなく、すべての外部参照を切断し、終了することができます。</span><span class="sxs-lookup"><span data-stu-id="44f38-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="44f38-128">高速シャットダウンを実行する必要がある MAPI クライアントは、 **IMAPIClientShutdown**インターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="44f38-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="44f38-129">MAPI クライアントは、任意の[imapisession](imapisessioniunknown.md)オブジェクトで IUnknown:: QueryInterface メソッドを呼び出すことによって、このインターフェイスへのポインターを取得できます。</span><span class="sxs-lookup"><span data-stu-id="44f38-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="44f38-130">MAPI クライアントは、 **IMAPIClientShutdown:: queryfastshutdown**メソッドを呼び出して、常に高速シャットダウンを開始します。</span><span class="sxs-lookup"><span data-stu-id="44f38-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="44f38-131">mapi サブシステムは、読み込み済みの mapi プロバイダーがクライアントの高速シャットダウンをサポートしているかどうかを確認することによって、mapi クライアントのクエリに応答します。</span><span class="sxs-lookup"><span data-stu-id="44f38-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="44f38-132">管理者は、Windows レジストリ設定を使用して、MAPI クライアントが高速シャットダウンを続行するために必要なプロバイダーサポートのレベルを判断するのに役立てることができます。</span><span class="sxs-lookup"><span data-stu-id="44f38-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="44f38-133">詳細については、「 [Fast Shutdown User Options](fast-shutdown-user-options.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44f38-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="44f38-134">高速シャットダウンを続行するには、クライアントは**IMAPIClientShutdown:: notifyprocessshutdown**メソッドを呼び出して、MAPI サブシステムにシャットダウンの意図を示します。</span><span class="sxs-lookup"><span data-stu-id="44f38-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="44f38-135">クライアントは**IMAPIClientShutdown::D ofastshutdown**メソッドを呼び出して、クライアントプロセスが直ちに終了したことを示します。</span><span class="sxs-lookup"><span data-stu-id="44f38-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="44f38-136">高速シャットダウンの詳細については、「[高速シャットダウンの概要](fast-shutdown-overview.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44f38-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="44f38-137">高速シャットダウンを正常に実行する方法については、「[ファストシャットダウンのベストプラクティス](best-practices-for-fast-shutdown.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44f38-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="44f38-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="44f38-138">See also</span></span>



[<span data-ttu-id="44f38-139">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="44f38-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="44f38-140">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="44f38-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

