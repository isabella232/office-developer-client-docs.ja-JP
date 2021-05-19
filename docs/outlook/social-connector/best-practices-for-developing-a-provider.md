---
title: プロバイダー開発のためのベスト プラクティス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: ソーシャル コネクタ 2013 (OSC) プロバイダーを開発する場合は、次Outlookに従う必要があります。
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425919"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="3e6a4-103">プロバイダー開発のためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="3e6a4-103">Best practices for developing a provider</span></span>

<span data-ttu-id="3e6a4-104">ソーシャル コネクタ 2013 (OSC) プロバイダーを開発する場合は、次Outlookに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="3e6a4-105">セキュリティ上の理由から、インターネット経由でサーバーと通信するプロバイダーは、HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) プロトコルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="3e6a4-106">それ以外の場合、転送中に電子メール アドレス、ソーシャル ネットワークアクティビティ、その他のユーザー データが傍受または公開されるリスクがあります。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="3e6a4-107">サードパーティのソーシャル ネットワーク用の OSC プロバイダーを開発する場合、プロバイダーはソーシャル ネットワークのサービス条件に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="3e6a4-108">プロバイダーダウンロード パッケージのサイズを最小限に抑えるために、C++ などのネイティブ コンパイラや、COM コンポーネントを構築できるその他のツールを使用してプロバイダーをビルドします。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="3e6a4-109">プロバイダーで、ソーシャル ネットワークに送信される一意のユーザー エージェントを作成して、プロバイダーがソーシャル ネットワークに対して行った通話を追跡します。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="3e6a4-110">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドは、プロバイダーの機能を取得するためにインターネットを通してソーシャル ネットワークを呼び出す方法に依存しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="3e6a4-111">たとえば、ユーザーはオフラインでOutlookできます。OSC が **GetCapabilities** を呼び出し、ネットワーク接続がない場合 **、GetCapabilities** 呼び出しは有効な機能 XML **を返しません**。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="3e6a4-112">ベスト プラクティスは、機能 XML **を** プロバイダーにリソースとして格納する方法です。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="3e6a4-113">OSC プロバイダーは、ソーシャル ネットワークへの呼び出しを大幅に生成できます。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="3e6a4-114">ソーシャル ネットワークのサービス条件に応じて、友人を Outlook フォルダーにキャッシュして、OSC からプロバイダーへの呼び出しの数を減らし、プロバイダーからソーシャル ネットワークに移動します。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="3e6a4-115">Office 2013 は、32 ビットバージョンと 64 ビット バージョンの両方で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="3e6a4-116">2010 Office以前Officeバージョンは、32 ビット バージョンでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="3e6a4-117">64 ビット Office 2013 の既定のインストールWindows 32 ビットです。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="3e6a4-118">64 ビット Office 2013 でインストールされている OSC の 64 ビット バージョンをサポートする場合は、64 ビット バージョンのプロバイダーもリリースする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e6a4-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3e6a4-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e6a4-119">See also</span></span>

- [<span data-ttu-id="3e6a4-120">OSC の一般的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="3e6a4-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="3e6a4-121">OSC XML スキーマを使用したプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="3e6a4-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="3e6a4-122">プロバイダーの展開</span><span class="sxs-lookup"><span data-stu-id="3e6a4-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="3e6a4-123">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="3e6a4-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

