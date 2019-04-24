---
title: サービスプロバイダーエントリポイント関数の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332992"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="1aa5c-103">サービスプロバイダーエントリポイント関数の実装</span><span class="sxs-lookup"><span data-stu-id="1aa5c-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="1aa5c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1aa5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1aa5c-105">すべてのサービスプロバイダー DLL には、MAPI が呼び出しを読み込むためのエントリポイント関数があります。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="1aa5c-106">このエントリポイント関数は[DllMain](https://msdn.microsoft.com/library/ms682583.aspx)と同じではないことに注意してください。 Win32 DLL エントリポイント関数です。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-106">Be aware that this entry point function is not the same as [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="1aa5c-107">プロバイダーの種類によっては、プロバイダーのエントリポイント関数が異なるプロトタイプに準拠しています。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="1aa5c-108">MAPI は、サービスプロバイダー用のさまざまなエントリポイント関数プロトタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="1aa5c-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="1aa5c-109">**Provider**</span></span>|<span data-ttu-id="1aa5c-110">**エントリポイント関数プロトタイプ**</span><span class="sxs-lookup"><span data-stu-id="1aa5c-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1aa5c-111">メッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="1aa5c-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="1aa5c-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="1aa5c-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="1aa5c-113">トランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="1aa5c-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="1aa5c-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="1aa5c-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="1aa5c-115">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1aa5c-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="1aa5c-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="1aa5c-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="1aa5c-117">これらのプロトタイプの機能の多くは、すべてのサービスプロバイダーの種類で同じです。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="1aa5c-118">アドレス帳、メッセージストア、およびトランスポートプロバイダーは、エントリポイント関数で次の2つの主要なタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="1aa5c-119">サービスプロバイダインターフェイス (SPI) のバージョンを調べて、MAPI がサービスプロバイダーが使用しているバージョンと互換性のあるバージョンを使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="1aa5c-120">MAPI spi バージョンを含む_lpulMAPIVer_パラメーターと、SPI バージョンを含む_lアウト providerver_パラメーターを使用して、チェックを実行します。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="1aa5c-121">これらのパラメーターは、次の3つの部分で構成される32ビットの符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="1aa5c-122">ビット 24 ~ 31 は、メジャーバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="1aa5c-123">ビット 16 ~ 23 は、マイナーバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="1aa5c-124">ビット 0 ~ 15 は、更新識別子を表します。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="1aa5c-125">メジャーバージョン番号はほとんど変更されませんが、MAPI が解放されて SPI が変更されるたびにマイナーバージョン番号が変更されます。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="1aa5c-126">更新識別子は、Microsoft の内部ビルドバージョンです。これは、開発プロセス中の変更を追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="1aa5c-127">MAPI は、Mapispi ヘッダーファイルに記録されている CURRENT_SPI_VERSION 定数を定義して、現在の SPI バージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="1aa5c-128">MAPI が使用しているバージョンより新しいバージョンの SPI を使用している場合は、エラー MAPI_E_VERSION でチェックに失敗します。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="1aa5c-129">プロバイダオブジェクトのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-129">Create an instance of a provider object.</span></span> <span data-ttu-id="1aa5c-130">プロバイダーは複数回開始および初期化される可能性があるため、この処理が行われるたびに新しいインスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="1aa5c-131">1つ以上のクライアントによって同時に使用されている複数のプロファイルにプロバイダーが表示されている場合、または1つのプロファイル内に複数回表示されている場合は、プロバイダーが複数回開始されます。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="1aa5c-132">エントリポイント関数のプロトタイプはプロバイダーの種類によって異なるため、プロバイダーオブジェクトの種類も異なります。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="1aa5c-133">アドレス帳プロバイダーを記述している場合は、 [IABProvider: IUnknown](iabprovideriunknown.md)を実装します。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="1aa5c-134">メッセージストアプロバイダーを記述している場合は、 [IMSProvider: IUnknown](imsprovideriunknown.md)を実装します。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="1aa5c-135">詳細については、「[メッセージストアプロバイダーの読み込み](loading-message-store-providers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="1aa5c-136">トランスポートプロバイダーを記述している場合は、 [ixpprovider: IUnknown](ixpprovideriunknown.md)を実装します。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="1aa5c-137">詳細については、「[トランスポートプロバイダーの初期化](initializing-the-transport-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1aa5c-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="1aa5c-138">See also</span></span>



[<span data-ttu-id="1aa5c-139">サービスプロバイダーの開始</span><span class="sxs-lookup"><span data-stu-id="1aa5c-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

