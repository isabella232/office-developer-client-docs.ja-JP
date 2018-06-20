---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: フォーム ベース認証を使用して、ソーシャル ネットワーク サイトにログオンします。
ms.openlocfilehash: 4af0301d5b619ce7f9ff54b97f54b4b00408a564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804372"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

フォーム ベース認証を使用して、ソーシャル ネットワーク サイトにログオンします。
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Parameters

_connectIn_
  
> [in]**Null**では、ログオン フォーム、またはこのメソッドが呼び出されたときに、ログオン プロセスのコンテキストによって、ログオンの資格情報を含む文字列を URL 文字列です。
    
_connectOut_
  
> [out]ログオン資格情報を含む文字列です。
    
## <a name="remarks"></a>備考

Outlook ソーシャル コネクタ (OSC) は、プロバイダーでは、フォーム ベース認証をサポートしていることを示している場合にのみ、 **LogonWeb**メソッドを呼び出します。 プロバイダーでは、**該当****機能**の XML ファイルで**useLogonWebAuth**を設定することでフォーム ベースの認証が必要なことを示します。 プロバイダーでは、 **useLogonWebAuth**が**false**に設定、OSC は基本認証を使用し、 [ISocialSession::Logon](isocialsession-logon.md)メソッドを呼び出します。 
  
フォーム ベース認証を使用して、ソーシャル ネットワーク サイトへのログオンでは、特定の順序で、 **LogonWeb**メソッドと[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md)メソッドを呼び出す必要があります。 
  
1. OSC は、最初に**LogonWeb**を呼び出す_connectIn_パラメーターに**null**を渡します。 
    
2. プロバイダーは、OSC のように、OSC_E_AUTH_ERROR エラーを発生させます。
    
3. OSC は、次に**GetLogonUrl**を呼び出します。
    
4. プロバイダーは、 **GetLogonUrl**メソッドでは、ログオン ページに適切な URL を返します。 
    
5. OSC では、 **GetLogonUrl**によって返される URL を使用して、フォーム ベースのログオン ページが表示します。 
    
6. OSC を呼び出して**LogonWeb** 2 回目、 _connectIn_パラメーターでのログオン フォームに URL を渡します。 
    
7. 認証が成功すると、プロバイダーは、OSC を_connectOut_パラメーターにログオン資格情報を返します。 認証が失敗した場合、プロバイダーは、OSC のように、OSC_E_AUTH_ERROR エラーを発生させます。 
    
OSC プロバイダーは、キャッシュされた資格情報を使用してログオンをサポートする場合は、XML の**機能**で**は** **useLogonCached**を指定します。 プロバイダーは、プロバイダーは、接続での格納に OSC をしようとしている_connectOut_の文字列に、ログオン資格情報を配置する必要があります。 OSC では、 _connectOut_の文字列は解釈されません。 OSC では、その**useLogonCached**が**true**を確認した後、OSC は、Windows レジストリに格納する前にセキュリティのための文字列を暗号化します。 OSC は、 [ISocialSession2::LogonCached](isocialsession2-logoncached.md)を呼び出すことによって、ソーシャル ネットワークへのログオンに 2 回目以降に、 _connectIn_パラメーターにこの文字列を渡します。 
  
エラー コードの詳細については、 [Outlook ソーシャル コネクタ プロバイダーのエラー コード](outlook-social-connector-provider-error-codes.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [ISocialSession: IUnknown](isocialsessioniunknown.md)
- [フォーム ベースの認証](forms-based-authentication.md)

