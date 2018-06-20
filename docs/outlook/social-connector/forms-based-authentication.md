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
# <a name="forms-based-authentication"></a>フォームベース認証

Outlook ソーシャル コネクタ (OSC) では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出します。 OSC では、返される機能を使用して、このソーシャル ネットワークにログオンしている Office ユーザーをサポートする方法を決定します。 

OSC プロバイダーがフォーム ベース認証をサポートしている**機能**の返された XML 内の**useLogonWebAuth**要素が示されている場合、OSC は、ソーシャル ネットワークにログオンするユーザーを許可するのには次の呼び出しシーケンスを作成できます。 
  
1. [ISocialProvider::Load](isocialprovider-load.md)&ndash; 、OSC プロバイダーを読み込みます。 
    
2. [ISocialProvider::Version](isocialprovider-version.md)&ndash;の OSC は、このソーシャル ネットワーク プロバイダーのバージョン番号を表す文字列を取得します。 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md)&ndash;の OSC は、ソーシャル ネットワークの名前を表す文字列を取得します。 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md)&ndash;の OSC は、ソーシャル ネットワークを表す変更不可の GUID を取得します。 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)&ndash;の OSC は、プロバイダーの機能を表していると、**機能**の要素のスキーマ定義に準拠する文字列を取得します。 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md)&ndash;の OSC は、ソーシャル ネットワーク サイトのアイコンを表すバイト配列を取得します。 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md)&ndash;の OSC は、 [ISocialSession](isocialsessioniunknown.md)インターフェイスを取得します。 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md)&ndash; 、OSC は、フォーム ベース認証でソーシャル ネットワーク サイトへのログオンを初期化します。 この最初のログオンの呼び出しに、OSC は**null**の場合、 _connectIn_パラメーターで渡されます。 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md)&ndash;の OSC は、web 認証の際に、ブラウザー ベースのフォームをユーザーに表示する URL を取得します。 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md)&ndash; 、OSC では、フォーム ベース認証を使用して、ソーシャル ネットワーク サイトへのログオンが完了するとします。 OSC は、2 回目、このメソッドを呼び出して、 _connectIn_パラメーターでプロバイダーにログオン フォームの URL を渡すことです。 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md)&ndash;の OSC は、ログオンしたユーザーを表す[ISocialProfile](isocialprovideriunknown.md)インターフェイスを取得します。 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md)&ndash;の OSC は、ソーシャル ネットワーク サイトの一意の識別子を表す文字列を取得します。 ネットワーク id はネットワーク名と同じにすることはできます。 
    
## <a name="see-also"></a>関連項目

- [機能のための XML](xml-for-capabilities.md)
- [OSC の典型的な呼び出しシーケンス](osc-typical-calling-sequences.md)

