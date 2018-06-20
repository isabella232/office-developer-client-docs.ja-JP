---
title: サービス プロバイダーのエントリ ポイント関数を実装します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 632aff9c0f6fc60ee9730b5e43667b5b610ae8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800920"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="bb4ec-103">サービス プロバイダーのエントリ ポイント関数を実装します。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="bb4ec-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb4ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb4ec-105">すべてのサービス プロバイダーの DLL には、それをロードするのには MAPI を呼び出す関数をポイントするエントリがあります。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="bb4ec-106">このエントリ ポイント関数は[DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx)、Win32 DLL エントリ ポイント関数の場合と同様に注意します。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-106">Be aware that this entry point function is not the same as [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="bb4ec-107">、プロバイダーの種類によって、プロバイダーのエントリ ポイント関数は、別のプロトタイプに準拠しています。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="bb4ec-108">MAPI では、サービス プロバイダーの別のエントリ ポイント関数のプロトタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="bb4ec-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="bb4ec-109">**Provider**</span></span>|<span data-ttu-id="bb4ec-110">**エントリ ポイント関数のプロトタイプ**</span><span class="sxs-lookup"><span data-stu-id="bb4ec-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb4ec-111">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="bb4ec-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="bb4ec-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="bb4ec-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="bb4ec-113">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="bb4ec-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="bb4ec-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="bb4ec-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="bb4ec-115">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="bb4ec-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="bb4ec-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="bb4ec-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="bb4ec-117">これらのプロトタイプ内の機能の多くは、すべてのサービス プロバイダーの種類に対して同じです。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="bb4ec-118">アドレス帳、メッセージ ・ ストア、およびトランスポート プロバイダーは、そのエントリ ポイント関数で次の 2 つの主要なタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="bb4ec-119">MAPI が、サービス ・ プロバイダーを使用しているバージョンと互換性のあるバージョンを使用していることを確認するサービス プロバイダー インターフェイス (SPI) のバージョンを確認してください。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="bb4ec-120">チェックを実行するのにには、SPI の MAPI のバージョンが含まれています、 _lpulMAPIVer_のパラメーターと、SPI のバージョンが含まれています、 _lpulProviderVer_のパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="bb4ec-121">これらのパラメーターは、32 ビット符号なし整数の 3 つの部分で構成されています。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="bb4ec-122">ビット 24 ~ 31 では、メジャー バージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="bb4ec-123">ビット 16 ~ 23 では、マイナー バージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="bb4ec-124">ビット 0 から 15 までは、更新プログラムの識別子を表します。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="bb4ec-125">メジャー バージョン番号が変更されたことはほとんどありませんが MAPI が解放され、SPI が変更されたときにマイナー バージョン番号の変更を。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="bb4ec-126">更新プログラム識別子は、Microsoft の内部ビルドのバージョンです。開発プロセス中に変更を追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="bb4ec-127">MAPI CURRENT_SPI_VERSION 定数を定義する SPI の現在のバージョンを示すために、Mapispi.h ヘッダー ファイルに記載されています。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="bb4ec-128">バージョンの MAPI を使用しているバージョンより新しい SPI を使用している場合は、MAPI_E_VERSION のエラー チェックを失敗します。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="bb4ec-129">プロバイダー オブジェクトのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-129">Create an instance of a provider object.</span></span> <span data-ttu-id="bb4ec-130">プロバイダーを起動し、複数回の初期化、ために、この現象が発生するたびに新しいインスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="bb4ec-131">プロバイダーが複数回開始、1 つまたは複数のクライアントによって同時に使用されている複数のプロファイルに表示されるとき、または 1 つのプロファイルで複数回表示されます。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="bb4ec-132">同様にエントリ ポイント関数のプロトタイプは、プロバイダーの種類によって異なる場合は、プロバイダー オブジェクトの型をも。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="bb4ec-133">アドレス帳プロバイダーを作成している場合は、実装[IABProvider: IUnknown](iabprovideriunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="bb4ec-134">メッセージ ストア プロバイダーを作成している場合は、実装[IMSProvider: IUnknown](imsprovideriunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="bb4ec-135">詳細については、[メッセージ ストア プロバイダーの読み込み](loading-message-store-providers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="bb4ec-136">トランスポート プロバイダーを作成している場合は、実装[IXPProvider: IUnknown](ixpprovideriunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="bb4ec-137">詳細については、[トランスポート プロバイダーの初期化](initializing-the-transport-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb4ec-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb4ec-138">See also</span></span>



[<span data-ttu-id="bb4ec-139">サービス プロバイダーを開始します。</span><span class="sxs-lookup"><span data-stu-id="bb4ec-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

