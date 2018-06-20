---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: キャッシュされた資格情報を使用して、ソーシャル ネットワーク サイトにログオンします。
ms.openlocfilehash: 098ccd2cd3a55affed683886ce1e297ed725475b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804379"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

キャッシュされた資格情報を使用して、ソーシャル ネットワーク サイトにログオンします。
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Parameters

_connectIn_
  
> [in]空の場合し、OSC が**LogonCached**を呼び出し、コンテキストによって、ログオンの資格情報を含む文字列です。
    
_userName_
  
> [in]ユーザー名を含む文字列です。
    
_password_
  
> [in]ユーザーのパスワードを含む文字列です。
    
_connectOut_
  
> [out]資格情報が含まれている不透明な文字列です。
    
## <a name="remarks"></a>備考

**機能** [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)から返された XML の**場合は true**として**useLogonCached**が設定されている場合にのみ、認証にこのメソッドが呼び出されます。
  
Outlook ソーシャル コネクタ (OSC) では、 **LogonCached**を呼び出し、 _connectIn_に空の文字列と空以外の_ユーザー名_と_パスワード_の文字列を渡します。 プロバイダーでは、ソーシャル ネットワークにログオンする_ユーザー名_と_パスワード_を使用して、認証が成功した場合は、OSC に不透明な_connectOut_パラメーターを返します。 認証が失敗した場合、プロバイダーは、OSC に OSC_E_LOGON_FAILURE エラーを返します。 
  
_ConnectOut_パラメーターでは、OSC に不透明な文字列し、は、パラメーターに渡される、 _connectIn_回目以降のソーシャル ネットワークにログオンするための OSC で。 プロバイダーは、プロバイダーが接続間にわたって格納 OSC _connectOut_文字列の任意の資格情報を配置する必要があります。 OSC では、 _connectOut_、内の文字列を解釈しません。 し、Windows レジストリに格納する前にセキュリティ上の目的の文字列を暗号化します。
  
## <a name="see-also"></a>関連項目

- [ISocialSession2: IUnknown](isocialsession2iunknown.md)

