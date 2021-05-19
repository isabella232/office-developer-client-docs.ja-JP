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
# <a name="forms-based-authentication"></a>フォームベース認証

ソーシャル Outlook (OSC) は[、ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出して、ソーシャル ネットワークの OSC プロバイダーの機能を決定します。 OSC は、返された機能を使用して、このソーシャル ネットワークにログオンOfficeユーザーをサポートする方法を決定します。 

返される機能 **XML** の **useLogonWebAuth** 要素が OSC プロバイダーがフォーム ベース認証をサポートしている場合、OSC は次の呼び出しシーケンスを実行して、ユーザーがソーシャル ネットワークにログオンできます。 
  
1. [ISocialProvider::Load](isocialprovider-load.md) &ndash; OSC はプロバイダーを読み込む。 
    
2. [ISocialProvider::Version](isocialprovider-version.md) &ndash; OSC は、このソーシャル ネットワークのプロバイダーのバージョン番号を表す文字列を取得します。 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; OSC は、ソーシャル ネットワーク名を表す文字列を取得します。 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; OSC は、ソーシャル ネットワークを表す変更できない GUID を取得します。 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; OSC は、プロバイダーの機能を表し、capabilities 要素のスキーマ定義に準拠する文字列 **を取得** します。 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; OSC は、ソーシャル ネットワーク サイトのアイコンを表すバイト配列を取得します。 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; OSC は [ISocialSession インターフェイスを取得](isocialsessioniunknown.md) します。 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OSC は、フォーム ベース認証によってソーシャル ネットワーク サイトへのログオンを初期化します。 この最初のログオン呼び出しでは、OSC は **connectIn** パラメーターに  _null を渡_ します。 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; OSC は、Web 認証中にブラウザー ベースのフォームをユーザーに表示する URL を取得します。 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; OSC は、フォーム ベース認証を使用してソーシャル ネットワーク サイトへのログオンを完了します。 OSC は、このメソッドを 2 回目に呼び出し、ログオン フォームの URL を  _connectIn_ パラメーターのプロバイダーに渡します。 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; OSC は、ログオン [しているユーザーを表す ISocialProfile](isocialprovideriunknown.md) インターフェイスを取得します。 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; OSC は、ソーシャル ネットワーク サイトの一意の識別子を表す文字列を取得します。 ネットワーク識別子は、ネットワーク名と同じものにできます。 
    
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)
- [OSC の一般的な呼び出しシーケンス](osc-typical-calling-sequences.md)

