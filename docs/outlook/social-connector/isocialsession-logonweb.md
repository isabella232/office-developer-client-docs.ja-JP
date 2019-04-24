---
title: i"alsessionalsessionlogonweb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: フォームベース認証を使用してソーシャルネットワークサイトにログオンします。
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335365"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

フォームベース認証を使用してソーシャルネットワークサイトにログオンします。
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>パラメーター

_//_
  
> 順番このメソッドが呼び出されたときのログオンプロセスのコンテキストに応じて、 **null**の文字列、web 上のログオンフォームへの URL、またはログオン資格情報を含む文字列。
    
_connectout_
  
> 読み上げログオン資格情報を含む文字列。
    
## <a name="remarks"></a>解説

Outlook Social Connector (.osc) は、プロバイダーがフォームベース認証をサポートしていることを示す場合にのみ、 **logonweb**メソッドを呼び出します。 プロバイダーは、XML の**機能**に対して**uselogonwebauth**を**true**に設定することにより、フォームベース認証が必要であることを示します。 プロバイダーが**uselogonwebauth**を**false**として設定している場合、.osc は基本認証を使用して、 [iime alsession:: Logon](isocialsession-logon.md)メソッドを呼び出します。 
  
フォームベース認証を使用してソーシャルネットワークサイトにログオンするには、特定の順序で**logonweb**および[isocial alsession:: getlogonurl](isocialsession-getlogonurl.md)メソッドを呼び出す必要があります。 
  
1. .osc は、最初に**logonweb**を呼び出し、 **null**を引数__ として指定します。 
    
2. プロバイダーは、.osc に OSC_E_AUTH_ERROR エラーを発生させます。
    
3. .osc の次のメソッドは、 **getlogonurl**を呼び出します。
    
4. プロバイダーは、 **getlogonurl**メソッドのログオンページに適切な URL を返します。 
    
5. .osc は、 **getlogonurl**によって返される url を使用して、フォームベースのログオンページを表示します。 
    
6. 次に、.osc は**logonweb**をもう一度呼び出し、その URL を "/入力" __ パラメーターでログオンフォームに渡します。 
    
7. 認証が成功すると、プロバイダーは、 _connectout_パラメーターのログオン資格情報を .osc に返します。 認証が失敗した場合、プロバイダーは .osc に OSC_E_AUTH_ERROR エラーを発生させます。 
    
.osc プロバイダーがキャッシュされた資格情報を使用したログ記録をサポートしている場合は、**機能**XML では**true**としてキャッシュされた**uselogoncached**指定します。 プロバイダーは、接続間に格納するために、プロバイダーが .osc を必要とする_connectout_文字列にログオン資格情報を配置する必要があります。 .osc は、 _connectout_文字列を解釈しません。 .osc は、 **uselogoncached**が**true**であることを確認した後、セキュリティのために文字列を暗号化してから Windows レジストリに保存します。 .osc は、 [ISocialSession2:: logoncached](isocialsession2-logoncached.md)を呼び出すことによって、ソーシャルネットワークへの次回のログオン時に、この文字列を引数として渡されます。 __ 
  
エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [フォームベース認証](forms-based-authentication.md)

