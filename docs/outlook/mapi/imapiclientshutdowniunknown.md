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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435335"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="06c49-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="06c49-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="06c49-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06c49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06c49-105">MAPI クライアントがクライアント プロセスの高速シャットダウンを実行できます。</span><span class="sxs-lookup"><span data-stu-id="06c49-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06c49-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="06c49-106">Header file:</span></span>  <br/> |<span data-ttu-id="06c49-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06c49-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="06c49-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="06c49-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="06c49-109">[IMAPISession](imapisessioniunknown.md) オブジェクト</span><span class="sxs-lookup"><span data-stu-id="06c49-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="06c49-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="06c49-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="06c49-111">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="06c49-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="06c49-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="06c49-112">Called by:</span></span>  <br/> |<span data-ttu-id="06c49-113">MAPI クライアント</span><span class="sxs-lookup"><span data-stu-id="06c49-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="06c49-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="06c49-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="06c49-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="06c49-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="06c49-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="06c49-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="06c49-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="06c49-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="06c49-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="06c49-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="06c49-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="06c49-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="06c49-120">読み込まれた MAPI プロバイダーによって提供される高速シャットダウンのサポートを MAPI サブシステムに照会します。</span><span class="sxs-lookup"><span data-stu-id="06c49-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="06c49-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="06c49-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="06c49-122">シャットダウンを続行する MAPI クライアントの意図を示します。</span><span class="sxs-lookup"><span data-stu-id="06c49-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="06c49-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="06c49-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="06c49-124">MAPI クライアントがクライアント プロセスを直ちに終了する意図を示します。</span><span class="sxs-lookup"><span data-stu-id="06c49-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06c49-125">注釈</span><span class="sxs-lookup"><span data-stu-id="06c49-125">Remarks</span></span>

<span data-ttu-id="06c49-126">高速シャットダウンの目的は、MAPI クライアントと、MAPI クライアントが MAPI 設定とデータを保存するアクティブな MAPI セッションを持つ読み込まれた MAPI プロバイダーを許可することです。</span><span class="sxs-lookup"><span data-stu-id="06c49-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="06c49-127">これにより、MAPI クライアントは、すべての外部参照を切断し、データ損失を引き起こすことなく終了できます。</span><span class="sxs-lookup"><span data-stu-id="06c49-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="06c49-128">高速シャットダウンを実行する必要がある MAPI クライアントは **、IMAPIClientShutdown インターフェイスを使用する必要** があります。</span><span class="sxs-lookup"><span data-stu-id="06c49-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="06c49-129">MAPI クライアントは [、IMAPISession](imapisessioniunknown.md) オブジェクトで IUnknown::QueryInterface メソッドを呼び出すことによって、このインターフェイスへのポインターを取得できます。</span><span class="sxs-lookup"><span data-stu-id="06c49-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="06c49-130">MAPI クライアントは **、IMAPIClientShutdown::QueryFastShutdown** メソッドを呼び出すことによって、常に高速シャットダウンを開始します。</span><span class="sxs-lookup"><span data-stu-id="06c49-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="06c49-131">MAPI サブシステムは、読み込まれた MAPI プロバイダーがクライアントの高速シャットダウンをサポートするかどうかを確認して、MAPI クライアントのクエリに応答します。</span><span class="sxs-lookup"><span data-stu-id="06c49-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="06c49-132">管理者は、Windows設定を使用して、MAPI クライアントが高速シャットダウンを続行するために必要なプロバイダー サポートのレベルを判断できます。</span><span class="sxs-lookup"><span data-stu-id="06c49-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="06c49-133">詳細については、「Fast [Shutdown User Options」を参照してください](fast-shutdown-user-options.md)。</span><span class="sxs-lookup"><span data-stu-id="06c49-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="06c49-134">高速シャットダウンを続行するために、クライアントは **IMAPIClientShutdown::NotifyProcessShutdown** メソッドを呼び出して、MAPI サブシステムにシャットダウンの意図を示します。</span><span class="sxs-lookup"><span data-stu-id="06c49-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="06c49-135">次に、クライアントは **IMAPIClientShutdown::D oFastShutdown** メソッドを呼び出して、クライアント プロセスが直ちに終了しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="06c49-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="06c49-136">高速シャットダウンの詳細については、「Fast [Shutdown Overview」を参照してください](fast-shutdown-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="06c49-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="06c49-137">高速シャットダウンを正常に実行する方法については、「高速シャットダウンの [ベスト プラクティス」を参照してください](best-practices-for-fast-shutdown.md)。</span><span class="sxs-lookup"><span data-stu-id="06c49-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06c49-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="06c49-138">See also</span></span>



[<span data-ttu-id="06c49-139">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="06c49-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="06c49-140">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="06c49-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

