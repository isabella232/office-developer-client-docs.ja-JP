---
title: 基本認証
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: ソーシャル Outlook (OSC) は、ISocialProvider::GetCapabilities メソッドを呼び出して、ソーシャル ネットワークの OSC プロバイダーの機能を決定します。
ms.openlocfilehash: 803fe6ae37bb408f8e3082e184317c4d19831906
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616258"
---
# <a name="basic-authentication"></a>基本認証

ソーシャル Outlook (OSC) は[、ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出して、ソーシャル ネットワークの OSC プロバイダーの機能を決定します。 OSC は、返された機能を使用して、このソーシャル ネットワークにログオンOfficeユーザーをサポートする方法を決定します。 返される機能 **XML** の **useLogonWebAuth** 要素が OSC プロバイダーが基本認証をサポートしている場合、OSC は次の呼び出しシーケンスを実行して、ユーザーがそのソーシャル ネットワークにログオンできます。 
  
1. [ISocialProvider::Load](isocialprovider-load.md) —OSC はプロバイダーを読み込む。 
    
2. [ISocialProvider::Version](isocialprovider-version.md) —OSC は、OSC プロバイダーのバージョン番号を表す文字列を取得します。 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —OSC は、ソーシャル ネットワーク名を表す文字列を取得します。 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —OSC は、ソーシャル ネットワークを表す変更できない GUID を取得します。 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —OSC は、プロバイダーの機能を表し、capabilities 要素のスキーマ定義に準拠する文字列 **を取得** します。 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —OSC は、ソーシャル ネットワーク サイトのアイコンを表すバイト配列を取得します。 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) —OSC は [ISocialSession インターフェイスを取得](isocialsessioniunknown.md) します。 
    
8. [ISocialSession::Logon](isocialsession-logon.md) —OSC は、指定されたユーザー名とパスワードを使用して、ユーザーをソーシャル ネットワーク サイトにログオンします。 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —OSC は、ログオンしているユーザーを表す [ISocialProfile](isocialprovideriunknown.md) インターフェイスを取得します。 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —OSC は、ソーシャル ネットワーク サイトの一意の識別子を表す文字列を取得します。 ネットワーク識別子は、ネットワーク名と同じものにできます。 
    
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)
- [OSC の一般的な呼び出しシーケンス](osc-typical-calling-sequences.md)

