---
title: プロバイダー開発のためのベスト プラクティス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: Outlook Social Connector 2013 (.osc) プロバイダーを開発するときは、以下の手順に従う必要があります。
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425919"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="362ac-103">プロバイダー開発のためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="362ac-103">Best practices for developing a provider</span></span>

<span data-ttu-id="362ac-104">Outlook Social Connector 2013 (.osc) プロバイダーを開発するときは、以下の手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="362ac-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="362ac-105">セキュリティ上の理由から、インターネットを介してサーバーと通信するプロバイダーは HTTPS (ハイパーテキスト転送プロトコル (HTTP) with Secure Socket Layer (SSL) プロトコル) を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="362ac-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="362ac-106">そうしないと、送信中に電子メールアドレス、ソーシャルネットワークアクティビティ、およびその他のユーザーデータが傍受または公開される危険性があります。</span><span class="sxs-lookup"><span data-stu-id="362ac-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="362ac-107">サードパーティのソーシャルネットワーク用の .osc プロバイダーを開発している場合は、プロバイダーがソーシャルネットワークのサービス利用規約に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="362ac-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="362ac-108">プロバイダーダウンロードパッケージのサイズを最小にするには、C++ などのネイティブコンパイラ、または COM コンポーネントを構築できる他のツールを使用して、プロバイダーを構築します。</span><span class="sxs-lookup"><span data-stu-id="362ac-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="362ac-109">プロバイダーで、ソーシャルネットワークに送信される一意のユーザーエージェントを作成し、プロバイダーがソーシャルネットワークに対して行った呼び出しを追跡します。</span><span class="sxs-lookup"><span data-stu-id="362ac-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="362ac-110">[imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドは、プロバイダーの機能を取得するためにインターネット経由でソーシャルネットワークを呼び出すことに依存しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="362ac-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="362ac-111">たとえば、ユーザーは Outlook をオフラインで起動できます。.osc が**getcapabilities**を呼び出し、ネットワーク接続がない場合、 **getcapabilities**呼び出しは有効な**機能**XML を返しません。</span><span class="sxs-lookup"><span data-stu-id="362ac-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="362ac-112">ベストプラクティスとして、プロバイダーのリソースとして**機能**XML を格納することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="362ac-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="362ac-113">.osc プロバイダーは、ソーシャルネットワークへの大量の呼び出しを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="362ac-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="362ac-114">ソーシャルネットワークのサービス条件によっては、友人を Outlook フォルダーにキャッシュして、.osc からプロバイダーへの呼び出し回数を減らし、プロバイダーからソーシャルネットワークに変換することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="362ac-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="362ac-115">Office 2013 は、32ビットと64ビットの両方のバージョンで利用できます。</span><span class="sxs-lookup"><span data-stu-id="362ac-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="362ac-116">office 2010 より前のバージョンの office は、32ビット版でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="362ac-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="362ac-117">64ビット Windows 上の Office 2013 の既定のインストールは、32ビットです。</span><span class="sxs-lookup"><span data-stu-id="362ac-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="362ac-118">64ビットの Office 2013 でインストールされた64ビットバージョンの .osc をサポートする予定の場合は、プロバイダーの64ビットバージョンもリリースする必要があります。</span><span class="sxs-lookup"><span data-stu-id="362ac-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="362ac-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="362ac-119">See also</span></span>

- [<span data-ttu-id="362ac-120">通常の呼び出しシーケンスの .osc</span><span class="sxs-lookup"><span data-stu-id="362ac-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="362ac-121">.osc XML スキーマを使用してプロバイダーを開発する</span><span class="sxs-lookup"><span data-stu-id="362ac-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="362ac-122">プロバイダーを展開する</span><span class="sxs-lookup"><span data-stu-id="362ac-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="362ac-123">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="362ac-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

