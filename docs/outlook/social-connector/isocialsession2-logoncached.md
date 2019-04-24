---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: キャッシュされた資格情報を使用してソーシャルネットワークサイトにログオンします。
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336506"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

キャッシュされた資格情報を使用してソーシャルネットワークサイトにログオンします。
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>パラメーター

_//_
  
> 順番この文字列は、.osc が**logoncached**を呼び出しているコンテキストに応じて、空の場合と、ログオン資格情報が含まれている場合があります。
    
_userName_
  
> 順番ユーザー名を含む文字列。
    
_password_
  
> 順番ユーザーのパスワードを含む文字列。
    
_connectout_
  
> 読み上げ資格情報を含む符号化文字列。
    
## <a name="remarks"></a>解説

このメソッドは、 [iime alprovider:: getcapabilities](isocialprovider-getcapabilities.md)によって返される**機能**XML で**uselogoncached**が**true**に設定されている場合にのみ、認証のために呼び出されます。
  
Outlook Social Connector (.osc) は、 **logoncached**を呼び出し、空の文字列を__ 指定します。ユーザー名とパスワードは空ではない_ユーザー名_と_パスワード_文字列を渡します。 プロバイダーは、ソーシャルネットワークにログオンするために_ユーザー名_と_パスワード_を使用し、認証が成功した場合は、不透明な_connectout_パラメーターを .osc に返します。 認証が失敗した場合、プロバイダーは、OSC_E_LOGON_FAILURE エラーを .osc に返します。 
  
_connectout_パラメーターは、.osc に対する不透明な文字列であり、.osc によっ__ てソーシャルネットワークにログオンするために、次に試行されたときに、このパラメーターに渡されます。 プロバイダーは、接続間に格納するために、プロバイダーが .osc を必要とするすべての資格情報を_connectout_文字列に配置する必要があります。 .osc は、 _connectout_の文字列を解釈しないで、セキュリティ上の理由で文字列を暗号化してから、Windows レジストリに保存します。
  
## <a name="see-also"></a>関連項目

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

