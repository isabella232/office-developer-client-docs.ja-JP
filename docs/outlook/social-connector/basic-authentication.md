---
title: 基本認証
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: Outlook ソーシャル コネクタ (OSC) では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する ISocialProvider::GetCapabilities メソッドを呼び出します。
ms.openlocfilehash: 8287133445a4e8fa928f6b7724ab41ca9b58baf9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804355"
---
# <a name="basic-authentication"></a><span data-ttu-id="309fc-103">基本認証</span><span class="sxs-lookup"><span data-stu-id="309fc-103">Basic authentication</span></span>

<span data-ttu-id="309fc-104">Outlook ソーシャル コネクタ (OSC) では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="309fc-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="309fc-105">OSC では、返される機能を使用して、このソーシャル ネットワークにログオンしている Office ユーザーをサポートする方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="309fc-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="309fc-106">OSC プロバイダーが基本認証をサポートしている**機能**の返された XML 内の**useLogonWebAuth**要素が示されている場合、OSC は、ソーシャル ネットワークにログオンするユーザーを許可するのには次の呼び出しシーケンスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="309fc-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="309fc-107">[ISocialProvider::Load](isocialprovider-load.md) -「OSC プロバイダーを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="309fc-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="309fc-108">[ISocialProvider::Version](isocialprovider-version.md) -「OSC は、OSC プロバイダーのバージョン番号を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="309fc-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="309fc-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) -「OSC は、ソーシャル ネットワークの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="309fc-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="309fc-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) -「OSC は、ソーシャル ネットワークを表す変更不可の GUID を取得します。</span><span class="sxs-lookup"><span data-stu-id="309fc-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="309fc-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -「OSC は、プロバイダー機能を表していると、**機能**要素のスキーマ定義に準拠する文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="309fc-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="309fc-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) -「OSC は、ソーシャル ネットワーク サイトのアイコン表すバイト配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="309fc-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="309fc-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) -「OSC は、 [ISocialSession](isocialsessioniunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="309fc-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="309fc-114">[ISocialSession::Logon](isocialsession-logon.md) -「OSC が指定されたユーザー名とパスワードを使用して、ソーシャル ネットワーク サイトにユーザーをログオンします。</span><span class="sxs-lookup"><span data-stu-id="309fc-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="309fc-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) -「OSC は、ログオンしたユーザーを表す[ISocialProfile](isocialprovideriunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="309fc-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="309fc-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) -「OSC は、ソーシャル ネットワーク サイト一意識別子を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="309fc-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="309fc-117">ネットワーク id はネットワーク名と同じにすることはできます。</span><span class="sxs-lookup"><span data-stu-id="309fc-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="309fc-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="309fc-118">See also</span></span>

- [<span data-ttu-id="309fc-119">機能のための XML</span><span class="sxs-lookup"><span data-stu-id="309fc-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="309fc-120">OSC の典型的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="309fc-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

