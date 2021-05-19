---
title: フォームベース認証
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: ソーシャル Outlook (OSC) は、ISocialProvider::GetCapabilities メソッドを呼び出して、ソーシャル ネットワークの OSC プロバイダーの機能を決定します。
ms.openlocfilehash: 420f19a8d7632f2ab9b093eb929ffe879f8a2fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435531"
---
# <a name="forms-based-authentication"></a><span data-ttu-id="b7e4e-103">フォームベース認証</span><span class="sxs-lookup"><span data-stu-id="b7e4e-103">Forms-based authentication</span></span>

<span data-ttu-id="b7e4e-104">ソーシャル Outlook (OSC) は[、ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出して、ソーシャル ネットワークの OSC プロバイダーの機能を決定します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="b7e4e-105">OSC は、返された機能を使用して、このソーシャル ネットワークにログオンOfficeユーザーをサポートする方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> 

<span data-ttu-id="b7e4e-106">返される機能 **XML** の **useLogonWebAuth** 要素が OSC プロバイダーがフォーム ベース認証をサポートしている場合、OSC は次の呼び出しシーケンスを実行して、ユーザーがソーシャル ネットワークにログオンできます。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports forms-based authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="b7e4e-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; OSC はプロバイダーを読み込む。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="b7e4e-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; OSC は、このソーシャル ネットワークのプロバイダーのバージョン番号を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; The OSC gets a string that represents the version number of the provider for this social network.</span></span> 
    
3. <span data-ttu-id="b7e4e-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; OSC は、ソーシャル ネットワーク名を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="b7e4e-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; OSC は、ソーシャル ネットワークを表す変更できない GUID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="b7e4e-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; OSC は、プロバイダーの機能を表し、capabilities 要素のスキーマ定義に準拠する文字列 **を取得** します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="b7e4e-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; OSC は、ソーシャル ネットワーク サイトのアイコンを表すバイト配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="b7e4e-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; OSC は [ISocialSession インターフェイスを取得](isocialsessioniunknown.md) します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="b7e4e-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OSC は、フォーム ベース認証によってソーシャル ネットワーク サイトへのログオンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC initializes logging on to the social network site by forms-based authentication.</span></span> <span data-ttu-id="b7e4e-115">この最初のログオン呼び出しでは、OSC は **connectIn** パラメーターに  _null を渡_ します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-115">For this initial logon call, the OSC passes **null** for the  _connectIn_ parameter.</span></span> 
    
9. <span data-ttu-id="b7e4e-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; OSC は、Web 認証中にブラウザー ベースのフォームをユーザーに表示する URL を取得します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; The OSC gets the URL to display a browser-based form to the user during web authentication.</span></span> 
    
10. <span data-ttu-id="b7e4e-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OSC は、フォーム ベース認証を使用してソーシャル ネットワーク サイトへのログオンを完了します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC completes the logon to the social network site by using forms-based authentication.</span></span> <span data-ttu-id="b7e4e-118">OSC は、このメソッドを 2 回目に呼び出し、ログオン フォームの URL を  _connectIn_ パラメーターのプロバイダーに渡します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-118">The OSC calls this method a second time, passing the URL of the logon form to the provider in the  _connectIn_ parameter.</span></span> 
    
11. <span data-ttu-id="b7e4e-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; OSC は、ログオン [しているユーザーを表す ISocialProfile](isocialprovideriunknown.md) インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
12. <span data-ttu-id="b7e4e-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; OSC は、ソーシャル ネットワーク サイトの一意の識別子を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="b7e4e-121">ネットワーク識別子は、ネットワーク名と同じものにできます。</span><span class="sxs-lookup"><span data-stu-id="b7e4e-121">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b7e4e-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7e4e-122">See also</span></span>

- [<span data-ttu-id="b7e4e-123">機能の XML</span><span class="sxs-lookup"><span data-stu-id="b7e4e-123">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="b7e4e-124">OSC の一般的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="b7e4e-124">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

