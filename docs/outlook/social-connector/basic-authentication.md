---
title: 基本認証
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: ソーシャル Outlook (OSC) は、ISocialProvider::GetCapabilities メソッドを呼び出して、ソーシャル ネットワークの OSC プロバイダーの機能を決定します。
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439927"
---
# <a name="basic-authentication"></a><span data-ttu-id="fa051-103">基本認証</span><span class="sxs-lookup"><span data-stu-id="fa051-103">Basic authentication</span></span>

<span data-ttu-id="fa051-104">ソーシャル Outlook (OSC) は[、ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出して、ソーシャル ネットワークの OSC プロバイダーの機能を決定します。</span><span class="sxs-lookup"><span data-stu-id="fa051-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="fa051-105">OSC は、返された機能を使用して、このソーシャル ネットワークにログオンOfficeユーザーをサポートする方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="fa051-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="fa051-106">返される機能 **XML** の **useLogonWebAuth** 要素が OSC プロバイダーが基本認証をサポートしている場合、OSC は次の呼び出しシーケンスを実行して、ユーザーがそのソーシャル ネットワークにログオンできます。</span><span class="sxs-lookup"><span data-stu-id="fa051-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="fa051-107">[ISocialProvider::Load](isocialprovider-load.md) —OSC はプロバイダーを読み込む。</span><span class="sxs-lookup"><span data-stu-id="fa051-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="fa051-108">[ISocialProvider::Version](isocialprovider-version.md) —OSC は、OSC プロバイダーのバージョン番号を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="fa051-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="fa051-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —OSC は、ソーシャル ネットワーク名を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="fa051-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="fa051-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —OSC は、ソーシャル ネットワークを表す変更できない GUID を取得します。</span><span class="sxs-lookup"><span data-stu-id="fa051-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="fa051-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —OSC は、プロバイダーの機能を表し、capabilities 要素のスキーマ定義に準拠する文字列 **を取得** します。</span><span class="sxs-lookup"><span data-stu-id="fa051-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="fa051-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —OSC は、ソーシャル ネットワーク サイトのアイコンを表すバイト配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="fa051-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="fa051-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —OSC は [ISocialSession インターフェイスを取得](isocialsessioniunknown.md) します。</span><span class="sxs-lookup"><span data-stu-id="fa051-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="fa051-114">[ISocialSession::Logon](isocialsession-logon.md) —OSC は、指定されたユーザー名とパスワードを使用して、ユーザーをソーシャル ネットワーク サイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="fa051-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="fa051-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —OSC は、ログオンしているユーザーを表す [ISocialProfile](isocialprovideriunknown.md) インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="fa051-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="fa051-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —OSC は、ソーシャル ネットワーク サイトの一意の識別子を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="fa051-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="fa051-117">ネットワーク識別子は、ネットワーク名と同じものにできます。</span><span class="sxs-lookup"><span data-stu-id="fa051-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fa051-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa051-118">See also</span></span>

- [<span data-ttu-id="fa051-119">機能の XML</span><span class="sxs-lookup"><span data-stu-id="fa051-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="fa051-120">OSC の一般的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="fa051-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

