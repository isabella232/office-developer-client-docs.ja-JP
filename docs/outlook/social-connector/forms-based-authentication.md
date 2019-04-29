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
# <a name="forms-based-authentication"></a>フォームベース認証

Outlook social Connector (.osc) は、 [imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出して、ソーシャルネットワークの .osc プロバイダーの機能を判別します。 .osc は、返された機能を使用して、このソーシャルネットワークにログオンしている Office ユーザーをサポートする方法を決定します。 

返された**機能**XML の**uselogonwebauth**要素が、.osc プロバイダーがフォームベース認証をサポートしていることを示している場合、.osc は、ユーザーがそのソーシャルネットワークにログオンできるようにするための次の呼び出し順序を作成できます。 
  
1. [iこの alprovider:: Load](isocialprovider-load.md)&ndash; .osc は、プロバイダーを読み込みます。 
    
2. [i/形式 alprovider:: Version](isocialprovider-version.md)&ndash; .osc は、このソーシャルネットワークのプロバイダーのバージョン番号を表す文字列を取得します。 
    
3. [i指定 alprovider::](isocialprovider-socialnetworkname.md) /指定&ndash; .osc は、ソーシャルネットワーク名を表す文字列を取得します。 
    
4. [iこの alprovider::](isocialprovider-socialnetworkguid.md) /"/"/"/"/"/"&ndash; .osc は、ソーシャルネットワークを表す不変の GUID を取得します。 
    
5. [isocialprovider:: getcapabilities](isocialprovider-getcapabilities.md)&ndash; .osc は、プロバイダーの機能を表す文字列を取得し、 **capabilities**要素のスキーマ定義に準拠します。 
    
6. [iこの alprovider::](isocialprovider-socialnetworkicon.md) /"/"&ndash; .osc は、ソーシャルネットワークサイトのアイコンを表すバイト配列を取得します。 
    
7. [isocialprovider:: getsession](isocialprovider-getsession.md)&ndash; .osc は、 [isocialsession](isocialsessioniunknown.md)インターフェイスを取得します。 
    
8. i/した[セッション:: logonweb](isocialsession-logonweb.md)&ndash; .osc は、フォームベース認証によってソーシャルネットワークサイトへのログ記録を初期化します。 この最初のログオン呼び出しの場合、.osc は、null __ を指定するパラメーターに対して**null**を渡します。 
    
9. [i、alsession:: getlogonurl](isocialsession-getlogonurl.md)&ndash; .osc は、web 認証中にユーザーにブラウザーベースのフォームを表示するための URL を取得します。 
    
10. i/した[セッション:: logonweb](isocialsession-logonweb.md)&ndash; .osc は、フォームベース認証を使用して、ソーシャルネットワークサイトへのログオンを完了します。 .osc は、このメソッドをもう一度呼び出して、ログオンフォームの URL を、入力された__ プロバイダーに渡します。 
    
11. [iGetLoggedOnUser alsession::](isocialsession-getloggedonuser.md)&ndash; .osc は、ログオンしているユーザーを表す[isocialprofile](isocialprovideriunknown.md)インターフェイスを取得します。 
    
12. [i入力 alsession:: getnetworkidentifier](isocialsession-getnetworkidentifier.md)&ndash; .osc は、ソーシャルネットワークサイトの一意の識別子を表す文字列を取得します。 ネットワーク識別子は、ネットワーク名に相当します。 
    
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)
- [通常の呼び出しシーケンスの .osc](osc-typical-calling-sequences.md)

