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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281222"
---
# <a name="basic-authentication"></a>基本認証

Outlook social Connector (.osc) は、 [imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出して、ソーシャルネットワークの .osc プロバイダーの機能を判別します。 .osc は、返された機能を使用して、このソーシャルネットワークにログオンしている Office ユーザーをサポートする方法を決定します。 返された**機能**XML の**uselogonwebauth**要素が、.osc プロバイダーが基本認証をサポートしていることを示している場合、.osc は、ユーザーがそのソーシャルネットワークにログオンできるようにするための次の呼び出しシーケンスを行うことができます。 
  
1. [ichanged alprovider:: Load](isocialprovider-load.md) — .osc は、プロバイダーを読み込みます。 
    
2. [ichanged alprovider:: Version](isocialprovider-version.md) -.osc は、.osc プロバイダーのバージョン番号を表す文字列を取得します。 
    
3. [i指定 alprovider::](isocialprovider-socialnetworkname.md) /"/"/"/"/"" は、ソーシャルネットワーク名を表す文字列を取得します。 
    
4. [ichanged alprovider::](isocialprovider-socialnetworkguid.md) //"/"/"/"/"は、ソーシャルネットワークを表す不変の guid を取得します。 
    
5. [i指定 alprovider:: getcapabilities](isocialprovider-getcapabilities.md) -.osc は、プロバイダーの機能を表す文字列を取得し、 **capabilities**要素のスキーマ定義に準拠しています。 
    
6. [ichanged alprovider::](isocialprovider-socialnetworkicon.md) //"/"/"/"/"ソーシャルネットワーク] サイトのアイコンを表すバイト配列を取得します。 
    
7. [ichanged alprovider:: getsession](isocialprovider-getsession.md) — .osc は、iな式[alsession](isocialsessioniunknown.md)インターフェイスを取得します。 
    
8. [ [i指定 alsession:: Logon](isocialsession-logon.md) ]: .osc は、指定されたユーザー名とパスワードを使用してソーシャルネットワークサイトにユーザーを記録します。 
    
9. [iGetLoggedOnUser alsession::](isocialsession-getloggedonuser.md) — .osc は、ログオンしているユーザーを表す[i alprofile](isocialprovideriunknown.md)インターフェイスを取得します。 
    
10. [i指定 alsession:: getnetworkidentifier](isocialsession-getnetworkidentifier.md) -.osc は、ソーシャルネットワークサイトの一意の識別子を表す文字列を取得します。 ネットワーク識別子は、ネットワーク名に相当します。 
    
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)
- [通常の呼び出しシーケンスの .osc](osc-typical-calling-sequences.md)

