---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: キャッシュされた資格情報を使用してソーシャル ネットワーク サイトにログオンします。
ms.openlocfilehash: 880484db2d5233e9a8bfe9cfd734d33d826dd4e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583017"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

キャッシュされた資格情報を使用してソーシャル ネットワーク サイトにログオンします。
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>パラメーター

_connectIn_
  
> [in]OSC が **LogonCached** を呼び出しているコンテキストに応じて、空またはログオン資格情報を含む文字列。
    
_userName_
  
> [in]ユーザー名を含む文字列。
    
_password_
  
> [in]ユーザーのパスワードを含む文字列。
    
_connectOut_
  
> [out]資格情報を含む不透明な文字列。
    
## <a name="remarks"></a>注釈

このメソッドは [、ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)によって返される機能 **XML** で **useLogonCached** が **true** に設定されている場合にのみ、認証のために呼び出されます。
  
このOutlookソーシャル コネクタ (OSC) は **LogonCached** を呼び出し _、connectIn_ および空でない _userName_ 文字列とパスワード文字列に空の文字列を _渡_ します。 プロバイダーは  _userName_  _とパスワード_ を使用してソーシャル ネットワークにログオンし、認証が成功した場合は不透明な  _connectOut_ パラメーターを OSC に返します。 認証に失敗した場合、プロバイダーは OSC にOSC_E_LOGON_FAILUREエラーを返します。 
  
_connectOut パラメーター_ は、OSC に対して不透明な文字列であり、OSC がソーシャル ネットワークにログオンしようとして以降に _connectIn_ パラメーターに渡されます。 プロバイダーは、OSC が接続間で格納する必要がある  _connectOut_ 文字列に資格情報を配置する必要があります。 OSC は _connectOut_ 内の文字列を解釈しません。また、セキュリティ上の目的で文字列を暗号化してから、Windowsします。
  
## <a name="see-also"></a>関連項目

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

