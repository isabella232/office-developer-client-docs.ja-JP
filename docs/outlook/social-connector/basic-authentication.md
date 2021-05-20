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

