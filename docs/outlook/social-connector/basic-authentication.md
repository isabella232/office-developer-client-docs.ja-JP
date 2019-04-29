---
title: 基本認証
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: 'Outlook social Connector (.osc) は、imethod alprovider:: getcapabilities メソッドを呼び出して、ソーシャルネットワークの .osc プロバイダーの機能を判別します。'
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439927"
---
# <a name="basic-authentication"></a><span data-ttu-id="e4aec-103">基本認証</span><span class="sxs-lookup"><span data-stu-id="e4aec-103">Basic authentication</span></span>

<span data-ttu-id="e4aec-104">Outlook social Connector (.osc) は、 [imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出して、ソーシャルネットワークの .osc プロバイダーの機能を判別します。</span><span class="sxs-lookup"><span data-stu-id="e4aec-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="e4aec-105">.osc は、返された機能を使用して、このソーシャルネットワークにログオンしている Office ユーザーをサポートする方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="e4aec-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="e4aec-106">返された**機能**XML の**uselogonwebauth**要素が、.osc プロバイダーが基本認証をサポートしていることを示している場合、.osc は、ユーザーがそのソーシャルネットワークにログオンできるようにするための次の呼び出しシーケンスを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e4aec-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="e4aec-107">[ichanged alprovider:: Load](isocialprovider-load.md) — .osc は、プロバイダーを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="e4aec-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="e4aec-108">[ichanged alprovider:: Version](isocialprovider-version.md) -.osc は、.osc プロバイダーのバージョン番号を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="e4aec-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="e4aec-109">[i指定 alprovider::](isocialprovider-socialnetworkname.md) /"/"/"/"/"" は、ソーシャルネットワーク名を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="e4aec-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="e4aec-110">[ichanged alprovider::](isocialprovider-socialnetworkguid.md) //"/"/"/"/"は、ソーシャルネットワークを表す不変の guid を取得します。</span><span class="sxs-lookup"><span data-stu-id="e4aec-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="e4aec-111">[i指定 alprovider:: getcapabilities](isocialprovider-getcapabilities.md) -.osc は、プロバイダーの機能を表す文字列を取得し、 **capabilities**要素のスキーマ定義に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="e4aec-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="e4aec-112">[ichanged alprovider::](isocialprovider-socialnetworkicon.md) //"/"/"/"/"ソーシャルネットワーク] サイトのアイコンを表すバイト配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="e4aec-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="e4aec-113">[ichanged alprovider:: getsession](isocialprovider-getsession.md) — .osc は、iな式[alsession](isocialsessioniunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="e4aec-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="e4aec-114">[ [i指定 alsession:: Logon](isocialsession-logon.md) ]: .osc は、指定されたユーザー名とパスワードを使用してソーシャルネットワークサイトにユーザーを記録します。</span><span class="sxs-lookup"><span data-stu-id="e4aec-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="e4aec-115">[iGetLoggedOnUser alsession::](isocialsession-getloggedonuser.md) — .osc は、ログオンしているユーザーを表す[i alprofile](isocialprovideriunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="e4aec-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="e4aec-116">[i指定 alsession:: getnetworkidentifier](isocialsession-getnetworkidentifier.md) -.osc は、ソーシャルネットワークサイトの一意の識別子を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="e4aec-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="e4aec-117">ネットワーク識別子は、ネットワーク名に相当します。</span><span class="sxs-lookup"><span data-stu-id="e4aec-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e4aec-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4aec-118">See also</span></span>

- [<span data-ttu-id="e4aec-119">機能の XML</span><span class="sxs-lookup"><span data-stu-id="e4aec-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="e4aec-120">通常の呼び出しシーケンスの .osc</span><span class="sxs-lookup"><span data-stu-id="e4aec-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

