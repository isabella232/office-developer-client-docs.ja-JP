---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a679d04f7697abbe0172105febf87082c0cd9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800704"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="c0159-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0159-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="c0159-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0159-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0159-105">MAPI プロバイダーが、シャット ダウンに応答できるように、MAPI クライアントの高速シャット ダウンの MAPI プロバイダーに通知するために MAPI サブシステムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c0159-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0159-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c0159-106">Header file:</span></span>  <br/> |<span data-ttu-id="c0159-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0159-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c0159-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="c0159-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="c0159-109">プロバイダー オブジェクト: [IXPProvider](ixpprovideriunknown.md)、 [IABProvider](iabprovideriunknown.md)、または[IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="c0159-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="c0159-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="c0159-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c0159-111">MAPI プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c0159-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="c0159-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c0159-112">Called by:</span></span>  <br/> |<span data-ttu-id="c0159-113">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="c0159-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="c0159-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="c0159-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c0159-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="c0159-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="c0159-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="c0159-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="c0159-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="c0159-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c0159-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="c0159-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c0159-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="c0159-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="c0159-120">クエリは高速シャット ダウンの MAPI プロバイダーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="c0159-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="c0159-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="c0159-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="c0159-122">MAPI プロバイダーをプロバイダーは、データ損失を防ぐための処置を行うことができるように、高速シャット ダウンを行う MAPI クライアントを送信することを示します。</span><span class="sxs-lookup"><span data-stu-id="c0159-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="c0159-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="c0159-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="c0159-124">示します MAPI プロバイダーに MAPI クライアントが、すぐに終了している MAPI プロバイダーがデータの損失を防ぐために加えられた変更を永続化できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c0159-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0159-125">注釈</span><span class="sxs-lookup"><span data-stu-id="c0159-125">Remarks</span></span>

<span data-ttu-id="c0159-126">高速シャット ダウンにより、MAPI クライアントは、短時間の処理を終了することを願って読み込まれていて、クライアント後 MAPI プロバイダーが、保存、MAPI の設定とデータです。</span><span class="sxs-lookup"><span data-stu-id="c0159-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="c0159-127">MAPI クライアントは常に高速シャット ダウンを開始して、MAPI のサブシステム読み込まれている MAPI プロバイダーから高速シャット ダウンをサポートするためにクエリを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0159-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="c0159-128">管理者は、すべての MAPI クライアントの高速シャット ダウンを許可する必要があるプロバイダーのサポートのレベルを指定するのにはユーザー レベルで、Windows のレジストリを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c0159-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="c0159-129">レジストリ設定の詳細については、[高速シャット ダウンのユーザー オプション](fast-shutdown-user-options.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c0159-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="c0159-130">ただし、データを失うことがなく正常に実行するのには高速シャット ダウンは、MAPI プロバイダーは、 **IMAPIProviderShutdown**インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0159-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="c0159-131">クライアントの高速シャット ダウンをサポートするために必要な MAPI プロバイダーは、MAPI サブシステムに、 **IMAPIProviderShutdown::QueryFastShutdown**メソッドで S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0159-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="c0159-132">MAPI プロバイダーが MAPI の設定とデータの保存に必要な操作を実行する必要があります MAPI サブシステムは、その後、 **IMAPIProviderShutdown::NotifyProcessShutdown**と**IMAPIProviderShutdown::DoFastShutdown**メソッドを呼び出しますと、クライアントの終了を準備します。</span><span class="sxs-lookup"><span data-stu-id="c0159-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="c0159-133">クライアントの高速シャット ダウンをサポートするために必要としない MAPI プロバイダーの**IMAPIProviderShutdown**インターフェイスを実装し、MAPI_E_NO_SUPPORT を返す**IMAPIProviderShutdown::QueryFastShutdown**メソッドがある必要がありますも。</span><span class="sxs-lookup"><span data-stu-id="c0159-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="c0159-134">MAPI クライアントとして outlook でこのすべての外部参照を終了する前に解放するまで待機するように Outlook が発生します。</span><span class="sxs-lookup"><span data-stu-id="c0159-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="c0159-135">によって**IMAPIProviderShutdown**インターフェイスを実装しない、高速シャット ダウンのレジストリ設定が必ずしもユーザーの Windows クライアントの高速シャット ダウンを防止します。</span><span class="sxs-lookup"><span data-stu-id="c0159-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="c0159-136">高速シャット ダウンのプロセスの詳細については、[高速シャット ダウンの概要](fast-shutdown-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c0159-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="c0159-137">高速シャット ダウンを正常に実行する方法の詳細については、[高速シャット ダウンのベスト ・ プラクティス](best-practices-for-fast-shutdown.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c0159-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0159-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="c0159-138">See also</span></span>



[<span data-ttu-id="c0159-139">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c0159-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="c0159-140">Mapi クライアントのシャット ダウン</span><span class="sxs-lookup"><span data-stu-id="c0159-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

