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
# <a name="basic-authentication"></a>基本認証

Outlook ソーシャル コネクタ (OSC) では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出します。 OSC では、返される機能を使用して、このソーシャル ネットワークにログオンしている Office ユーザーをサポートする方法を決定します。 OSC プロバイダーが基本認証をサポートしている**機能**の返された XML 内の**useLogonWebAuth**要素が示されている場合、OSC は、ソーシャル ネットワークにログオンするユーザーを許可するのには次の呼び出しシーケンスを作成できます。 
  
1. [ISocialProvider::Load](isocialprovider-load.md) -「OSC プロバイダーを読み込みます。 
    
2. [ISocialProvider::Version](isocialprovider-version.md) -「OSC は、OSC プロバイダーのバージョン番号を表す文字列を取得します。 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) -「OSC は、ソーシャル ネットワークの名前を表す文字列を取得します。 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) -「OSC は、ソーシャル ネットワークを表す変更不可の GUID を取得します。 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -「OSC は、プロバイダー機能を表していると、**機能**要素のスキーマ定義に準拠する文字列を取得します。 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) -「OSC は、ソーシャル ネットワーク サイトのアイコン表すバイト配列を取得します。 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) -「OSC は、 [ISocialSession](isocialsessioniunknown.md)インターフェイスを取得します。 
    
8. [ISocialSession::Logon](isocialsession-logon.md) -「OSC が指定されたユーザー名とパスワードを使用して、ソーシャル ネットワーク サイトにユーザーをログオンします。 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) -「OSC は、ログオンしたユーザーを表す[ISocialProfile](isocialprovideriunknown.md)インターフェイスを取得します。 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) -「OSC は、ソーシャル ネットワーク サイト一意識別子を表す文字列を取得します。 ネットワーク id はネットワーク名と同じにすることはできます。 
    
## <a name="see-also"></a>関連項目

- [機能のための XML](xml-for-capabilities.md)
- [OSC の典型的な呼び出しシーケンス](osc-typical-calling-sequences.md)

