---
title: プロバイダーを開発するためのベスト プラクティス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: Outlook ソーシャル コネクタ 2013 (OSC) プロバイダーを開発する場合は、以下のプラクティスに従う必要があります。
ms.openlocfilehash: a6ee9d54f33bbc855d178aba844a8f65ec92f964
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804327"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="f9bfe-103">プロバイダーを開発するためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="f9bfe-103">Best practices for developing a provider</span></span>

<span data-ttu-id="f9bfe-104">Outlook ソーシャル コネクタ 2013 (OSC) プロバイダーを開発する場合は、以下のプラクティスに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="f9bfe-105">セキュリティ上の理由から、インターネット経由でサーバーと通信するプロバイダーは、(ハイパー テキスト転送プロトコル (HTTP) をセキュリティで保護されたソケット レイヤー (SSL)) を HTTPS プロトコルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="f9bfe-106">それ以外の場合は、リスクそのメール アドレス、ソーシャル ネットワーク活動、およびその他のユーザーのデータを傍受または送信中に公開される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="f9bfe-107">OSC プロバイダーのサード パーティ製のソーシャル ネットワークを開発する場合、プロバイダーがサービスのソーシャル ネットワークの条項に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="f9bfe-108">プロバイダーのダウンロード パッケージのサイズを最小限に抑えるには、C++ または COM コンポーネントを作成することができますが、他のツールなどのネイティブ コンパイラを使用してプロバイダーを構築します。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="f9bfe-109">、プロバイダーでは、ソーシャル ネットワーク プロバイダーからの呼び出しを追跡するためにソーシャル ネットワークに送信される一意のユーザー エージェントを作成します。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="f9bfe-110">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドは、プロバイダーの機能を取得するのにはインターネット経由でソーシャル ネットワークを呼び出すことに依存させないでください。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="f9bfe-111">など、ユーザーが Outlook をオフラインで起動します。OSC は、 **GetCapabilities**を呼び出して、ネットワークが接続されていない場合は、 **GetCapabilities**の呼び出しには、有効な XML**の機能**は返されません。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="f9bfe-112">プロバイダーでリソースとして XML の**機能**を格納することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="f9bfe-113">OSC プロバイダーでは、ソーシャル ネットワークへの呼び出しの膨大な量を生成できます。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="f9bfe-114">によって、ソーシャル ネットワークのサービスの条件によって、キャッシュ プロバイダーに OSC からと、さらに、ソーシャル ネットワーク プロバイダーからの呼び出しの数を減らすために、Outlook フォルダーに友人を検討します。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="f9bfe-115">Office 2013 は、32 ビットと 64 ビットの両方のバージョンで使用できます。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="f9bfe-116">Office 2010 の前に Office のバージョンは、32 ビット バージョンでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="f9bfe-117">Office 2013 の 64 ビット Windows での既定のインストールは、32 ビットです。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="f9bfe-118">64 ビットの Office 2013 がインストールされている OSC の 64 ビット バージョンをサポートする場合は、プロバイダーの 64 ビット バージョンをリリースする必要がありますもします。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f9bfe-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="f9bfe-119">See also</span></span>

- [<span data-ttu-id="f9bfe-120">OSC の典型的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="f9bfe-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="f9bfe-121">OSC の XML スキーマを使用してプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="f9bfe-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="f9bfe-122">プロバイダーを展開します。</span><span class="sxs-lookup"><span data-stu-id="f9bfe-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="f9bfe-123">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="f9bfe-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

