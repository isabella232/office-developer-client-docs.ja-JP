---
title: フォームベース認証
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: 'Outlook social Connector (.osc) は、imethod alprovider:: getcapabilities メソッドを呼び出して、ソーシャルネットワークの .osc プロバイダーの機能を判別します。'
ms.openlocfilehash: 420f19a8d7632f2ab9b093eb929ffe879f8a2fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435531"
---
# <a name="forms-based-authentication"></a><span data-ttu-id="2dff4-103">フォームベース認証</span><span class="sxs-lookup"><span data-stu-id="2dff4-103">Forms-based authentication</span></span>

<span data-ttu-id="2dff4-104">Outlook social Connector (.osc) は、 [imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出して、ソーシャルネットワークの .osc プロバイダーの機能を判別します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="2dff4-105">.osc は、返された機能を使用して、このソーシャルネットワークにログオンしている Office ユーザーをサポートする方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> 

<span data-ttu-id="2dff4-106">返された**機能**XML の**uselogonwebauth**要素が、.osc プロバイダーがフォームベース認証をサポートしていることを示している場合、.osc は、ユーザーがそのソーシャルネットワークにログオンできるようにするための次の呼び出し順序を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2dff4-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports forms-based authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="2dff4-107">[iこの alprovider:: Load](isocialprovider-load.md)&ndash; .osc は、プロバイダーを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="2dff4-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="2dff4-108">[i/形式 alprovider:: Version](isocialprovider-version.md)&ndash; .osc は、このソーシャルネットワークのプロバイダーのバージョン番号を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; The OSC gets a string that represents the version number of the provider for this social network.</span></span> 
    
3. <span data-ttu-id="2dff4-109">[i指定 alprovider::](isocialprovider-socialnetworkname.md) /指定&ndash; .osc は、ソーシャルネットワーク名を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="2dff4-110">[iこの alprovider::](isocialprovider-socialnetworkguid.md) /"/"/"/"/"/"&ndash; .osc は、ソーシャルネットワークを表す不変の GUID を取得します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="2dff4-111">[isocialprovider:: getcapabilities](isocialprovider-getcapabilities.md)&ndash; .osc は、プロバイダーの機能を表す文字列を取得し、 **capabilities**要素のスキーマ定義に準拠します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="2dff4-112">[iこの alprovider::](isocialprovider-socialnetworkicon.md) /"/"&ndash; .osc は、ソーシャルネットワークサイトのアイコンを表すバイト配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="2dff4-113">[isocialprovider:: getsession](isocialprovider-getsession.md)&ndash; .osc は、 [isocialsession](isocialsessioniunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="2dff4-114">i/した[セッション:: logonweb](isocialsession-logonweb.md)&ndash; .osc は、フォームベース認証によってソーシャルネットワークサイトへのログ記録を初期化します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC initializes logging on to the social network site by forms-based authentication.</span></span> <span data-ttu-id="2dff4-115">この最初のログオン呼び出しの場合、.osc は、null __ を指定するパラメーターに対して**null**を渡します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-115">For this initial logon call, the OSC passes **null** for the  _connectIn_ parameter.</span></span> 
    
9. <span data-ttu-id="2dff4-116">[i、alsession:: getlogonurl](isocialsession-getlogonurl.md)&ndash; .osc は、web 認証中にユーザーにブラウザーベースのフォームを表示するための URL を取得します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; The OSC gets the URL to display a browser-based form to the user during web authentication.</span></span> 
    
10. <span data-ttu-id="2dff4-117">i/した[セッション:: logonweb](isocialsession-logonweb.md)&ndash; .osc は、フォームベース認証を使用して、ソーシャルネットワークサイトへのログオンを完了します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC completes the logon to the social network site by using forms-based authentication.</span></span> <span data-ttu-id="2dff4-118">.osc は、このメソッドをもう一度呼び出して、ログオンフォームの URL を、入力された__ プロバイダーに渡します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-118">The OSC calls this method a second time, passing the URL of the logon form to the provider in the  _connectIn_ parameter.</span></span> 
    
11. <span data-ttu-id="2dff4-119">[iGetLoggedOnUser alsession::](isocialsession-getloggedonuser.md)&ndash; .osc は、ログオンしているユーザーを表す[isocialprofile](isocialprovideriunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
12. <span data-ttu-id="2dff4-120">[i入力 alsession:: getnetworkidentifier](isocialsession-getnetworkidentifier.md)&ndash; .osc は、ソーシャルネットワークサイトの一意の識別子を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="2dff4-121">ネットワーク識別子は、ネットワーク名に相当します。</span><span class="sxs-lookup"><span data-stu-id="2dff4-121">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2dff4-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="2dff4-122">See also</span></span>

- [<span data-ttu-id="2dff4-123">機能の XML</span><span class="sxs-lookup"><span data-stu-id="2dff4-123">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="2dff4-124">通常の呼び出しシーケンスの .osc</span><span class="sxs-lookup"><span data-stu-id="2dff4-124">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

