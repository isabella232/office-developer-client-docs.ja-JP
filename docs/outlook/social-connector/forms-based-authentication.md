---
title: フォームベース認証
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: Outlook ソーシャル コネクタ (OSC) では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する ISocialProvider::GetCapabilities メソッドを呼び出します。
ms.openlocfilehash: bf6534b72af7db92e02bed74f2028a086b26cbcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804343"
---
# <a name="forms-based-authentication"></a><span data-ttu-id="dfd2b-103">フォームベース認証</span><span class="sxs-lookup"><span data-stu-id="dfd2b-103">Forms-based authentication</span></span>

<span data-ttu-id="dfd2b-104">Outlook ソーシャル コネクタ (OSC) では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="dfd2b-105">OSC では、返される機能を使用して、このソーシャル ネットワークにログオンしている Office ユーザーをサポートする方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> 

<span data-ttu-id="dfd2b-106">OSC プロバイダーがフォーム ベース認証をサポートしている**機能**の返された XML 内の**useLogonWebAuth**要素が示されている場合、OSC は、ソーシャル ネットワークにログオンするユーザーを許可するのには次の呼び出しシーケンスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports forms-based authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="dfd2b-107">[ISocialProvider::Load](isocialprovider-load.md)&ndash; 、OSC プロバイダーを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="dfd2b-108">[ISocialProvider::Version](isocialprovider-version.md)&ndash;の OSC は、このソーシャル ネットワーク プロバイダーのバージョン番号を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; The OSC gets a string that represents the version number of the provider for this social network.</span></span> 
    
3. <span data-ttu-id="dfd2b-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md)&ndash;の OSC は、ソーシャル ネットワークの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="dfd2b-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md)&ndash;の OSC は、ソーシャル ネットワークを表す変更不可の GUID を取得します。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="dfd2b-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)&ndash;の OSC は、プロバイダーの機能を表していると、**機能**の要素のスキーマ定義に準拠する文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="dfd2b-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md)&ndash;の OSC は、ソーシャル ネットワーク サイトのアイコンを表すバイト配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="dfd2b-113">[ISocialProvider::GetSession](isocialprovider-getsession.md)&ndash;の OSC は、 [ISocialSession](isocialsessioniunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="dfd2b-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md)&ndash; 、OSC は、フォーム ベース認証でソーシャル ネットワーク サイトへのログオンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC initializes logging on to the social network site by forms-based authentication.</span></span> <span data-ttu-id="dfd2b-115">この最初のログオンの呼び出しに、OSC は**null**の場合、 _connectIn_パラメーターで渡されます。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-115">For this initial logon call, the OSC passes **null** for the  _connectIn_ parameter.</span></span> 
    
9. <span data-ttu-id="dfd2b-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md)&ndash;の OSC は、web 認証の際に、ブラウザー ベースのフォームをユーザーに表示する URL を取得します。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; The OSC gets the URL to display a browser-based form to the user during web authentication.</span></span> 
    
10. <span data-ttu-id="dfd2b-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md)&ndash; 、OSC では、フォーム ベース認証を使用して、ソーシャル ネットワーク サイトへのログオンが完了するとします。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC completes the logon to the social network site by using forms-based authentication.</span></span> <span data-ttu-id="dfd2b-118">OSC は、2 回目、このメソッドを呼び出して、 _connectIn_パラメーターでプロバイダーにログオン フォームの URL を渡すことです。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-118">The OSC calls this method a second time, passing the URL of the logon form to the provider in the  _connectIn_ parameter.</span></span> 
    
11. <span data-ttu-id="dfd2b-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md)&ndash;の OSC は、ログオンしたユーザーを表す[ISocialProfile](isocialprovideriunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
12. <span data-ttu-id="dfd2b-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md)&ndash;の OSC は、ソーシャル ネットワーク サイトの一意の識別子を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="dfd2b-121">ネットワーク id はネットワーク名と同じにすることはできます。</span><span class="sxs-lookup"><span data-stu-id="dfd2b-121">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="dfd2b-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="dfd2b-122">See also</span></span>

- [<span data-ttu-id="dfd2b-123">機能のための XML</span><span class="sxs-lookup"><span data-stu-id="dfd2b-123">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="dfd2b-124">OSC の典型的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="dfd2b-124">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

