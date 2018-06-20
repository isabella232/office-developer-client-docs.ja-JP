---
title: ISocialSessionLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: 指定されたユーザー名とパスワードを使用して、ソーシャル ネットワーク サイトにログオンします。
ms.openlocfilehash: d7a79767f3726f9748ea48839f1e190af2e9ec74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804367"
---
# <a name="isocialsessionlogon"></a>ISocialSession::Logon

指定されたユーザー名とパスワードを使用して、ソーシャル ネットワーク サイトにログオンします。
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a>Parameters

_ユーザー名_
  
> [in]ログオンするユーザー名を含む文字列です。
    
_password_
  
> [in]ログオン時にパスワードを含む文字列です。
    
## <a name="see-also"></a>関連項目

- [ISocialSession: IUnknown](isocialsessioniunknown.md)

