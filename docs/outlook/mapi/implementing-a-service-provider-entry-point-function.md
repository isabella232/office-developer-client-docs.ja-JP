---
title: サービス プロバイダーエントリ ポイント関数の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332992"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="666ad-103">サービス プロバイダーエントリ ポイント関数の実装</span><span class="sxs-lookup"><span data-stu-id="666ad-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="666ad-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="666ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="666ad-105">すべてのサービス プロバイダー DLL には、MAPI が呼び出して読み込むエントリ ポイント関数があります。</span><span class="sxs-lookup"><span data-stu-id="666ad-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="666ad-106">このエントリ ポイント関数は [、Win32](https://msdn.microsoft.com/library/ms682583.aspx)DLL エントリ ポイント関数である DllMain と同じではありません。</span><span class="sxs-lookup"><span data-stu-id="666ad-106">Be aware that this entry point function is not the same as [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="666ad-107">プロバイダーの種類に応じて、プロバイダーエントリ ポイント関数は別のプロトタイプに準拠します。</span><span class="sxs-lookup"><span data-stu-id="666ad-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="666ad-108">MAPI では、サービス プロバイダー用に異なるエントリ ポイント関数プロトタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="666ad-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="666ad-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="666ad-109">**Provider**</span></span>|<span data-ttu-id="666ad-110">**エントリ ポイント関数のプロトタイプ**</span><span class="sxs-lookup"><span data-stu-id="666ad-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="666ad-111">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="666ad-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="666ad-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="666ad-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="666ad-113">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="666ad-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="666ad-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="666ad-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="666ad-115">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="666ad-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="666ad-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="666ad-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="666ad-117">これらのプロトタイプの機能の多くが、すべてのサービス プロバイダーの種類で同じです。</span><span class="sxs-lookup"><span data-stu-id="666ad-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="666ad-118">アドレス帳、メッセージ ストア、およびトランスポート プロバイダーは、エントリ ポイント関数で次の 2 つの主要なタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="666ad-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="666ad-119">サービス プロバイダー インターフェイス (SPI) のバージョンを確認して、MAPI がサービス プロバイダーが使用しているバージョンと互換性のあるバージョンを使用している必要があります。</span><span class="sxs-lookup"><span data-stu-id="666ad-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="666ad-120">チェックを実行するには、MAPI SPI バージョンを含む  _lpulMAPIVer_ パラメーターと、SPI バージョンを含む  _lpulProviderVer_ パラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="666ad-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="666ad-121">これらのパラメーターは、3 つの部分で構成される 32 ビット符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="666ad-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="666ad-122">ビット 24 ~ 31 はメジャー バージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="666ad-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="666ad-123">ビット 16 ~ 23 はマイナー バージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="666ad-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="666ad-124">ビット 0 ~ 15 は更新識別子を表します。</span><span class="sxs-lookup"><span data-stu-id="666ad-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="666ad-125">メジャー バージョン番号はほとんど変更されませんが、MAPI がリリースされ、SPI が変更されるたびにマイナー バージョン番号が変更されます。</span><span class="sxs-lookup"><span data-stu-id="666ad-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="666ad-126">更新プログラムの識別子は、Microsoft の内部ビルド バージョンです。開発プロセス中の変更を追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="666ad-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="666ad-127">MAPI は、現在CURRENT_SPI_VERSION SPI バージョンを示すために Mapispi.h ヘッダー ファイルに記載されている定数を定義します。</span><span class="sxs-lookup"><span data-stu-id="666ad-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="666ad-128">MAPI が使用しているバージョンMAPI_E_VERSIONバージョンの SPI を使用している場合は、エラー メッセージを表示してチェックを失敗します。</span><span class="sxs-lookup"><span data-stu-id="666ad-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="666ad-129">プロバイダー オブジェクトのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="666ad-129">Create an instance of a provider object.</span></span> <span data-ttu-id="666ad-130">プロバイダーを複数回開始および初期化することができますので、これが発生する度に新しいインスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="666ad-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="666ad-131">プロバイダーは、1 つ以上のクライアントが同時に使用している複数のプロファイルに表示される場合、または 1 つのプロファイルに複数回表示される場合に複数回開始されます。</span><span class="sxs-lookup"><span data-stu-id="666ad-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="666ad-132">エントリ ポイント関数のプロトタイプがプロバイダーの種類によって異なるのと同様に、プロバイダー オブジェクトの種類も異なります。</span><span class="sxs-lookup"><span data-stu-id="666ad-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="666ad-133">アドレス帳プロバイダーを作成する場合は [、IABProvider : IUnknown を実装します](iabprovideriunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="666ad-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="666ad-134">メッセージ ストア プロバイダーを作成する場合は [、IMSProvider : IUnknown を実装します](imsprovideriunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="666ad-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="666ad-135">詳細については、「メッセージ ストア プロバイダー [の読み込み」を参照してください](loading-message-store-providers.md)。</span><span class="sxs-lookup"><span data-stu-id="666ad-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="666ad-136">トランスポート プロバイダーを作成する場合は [、IXPProvider : IUnknown を実装します](ixpprovideriunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="666ad-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="666ad-137">詳細については、「トランスポート プロバイダーの [初期化」を参照してください](initializing-the-transport-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="666ad-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="666ad-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="666ad-138">See also</span></span>



[<span data-ttu-id="666ad-139">サービス プロバイダーの開始</span><span class="sxs-lookup"><span data-stu-id="666ad-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

