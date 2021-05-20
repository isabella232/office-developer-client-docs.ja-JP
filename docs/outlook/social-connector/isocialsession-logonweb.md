---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: フォーム ベース認証を使用してソーシャル ネットワーク サイトにログオンします。
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430337"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

フォーム ベース認証を使用してソーシャル ネットワーク サイトにログオンします。
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>パラメーター

_connectIn_
  
> [in]null の文字列、Web 上のログオン フォームへの URL、またはこのメソッドが呼び出された場合のログオン プロセスのコンテキストに応じて、ログオン資格情報を含む文字列。
    
_connectOut_
  
> [out]ログオン資格情報を含む文字列。
    
## <a name="remarks"></a>注釈

このOutlookソーシャル コネクタ (OSC) は、プロバイダーがフォーム ベース認証をサポートすると示している場合にのみ **LogonWeb** メソッドを呼び出します。 プロバイダーは、機能の XML で **useLogonWebAuth** を **true** に設定して、フォーム ベースの認証を必要と **します**。 プロバイダーが **useLogonWebAuth** を **false** に設定すると、OSC は基本認証を使用し [、ISocialSession::Logon メソッドを呼び出](isocialsession-logon.md) します。 
  
フォーム ベース認証を使用してソーシャル ネットワーク サイトにログオンするには **、LogonWeb** メソッドと [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) メソッドを特定の順序で呼び出す必要があります。 
  
1. OSC は **LogonWeb を初めて** 呼び出し **、connectIn** パラメーターに null  _を渡_ します。 
    
2. プロバイダーは、OSC OSC_E_AUTH_ERRORエラーを発生します。
    
3. OSC は次に **GetLogonUrl を呼び出します**。
    
4. プロバイダーは **、GetLogonUrl** メソッドのログオン ページに適切な URL を返します。 
    
5. OSC は **、GetLogonUrl** によって返される URL を使用して、フォーム ベースのログオン ページを表示します。 
    
6. その後、OSC は LogonWeb を **2** 回目に呼び出し  _、connectIn_ パラメーターのログオン フォームに URL を渡します。 
    
7. 認証が成功した場合、プロバイダーは  _connectOut_ パラメーターのログオン資格情報を OSC に返します。 認証に失敗した場合、プロバイダーは OSC OSC_E_AUTH_ERRORエラーを発生します。 
    
OSC プロバイダーがキャッシュされた資格情報の使用によるログオンをサポートしている場合は、機能 XML で **useLogonCached** を **true** **として指定** します。 プロバイダーは、OSC が接続間で格納する必要がある  _connectOut_ 文字列にログオン資格情報を配置する必要があります。 OSC は  _connectOut 文字列を解釈_ しない。 OSC が **useLogonCached** がtrue であるのを確認した後、OSC はセキュリティのために文字列を暗号化してから、その文字列をレジストリWindowsします。 OSC は [、ISocialSession2::LogonCached](isocialsession2-logoncached.md)を呼び出してソーシャル ネットワークにログオンしようとして、この文字列を _connectIn_ パラメーターに渡します。 
  
エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [フォーム ベース認証](forms-based-authentication.md)

