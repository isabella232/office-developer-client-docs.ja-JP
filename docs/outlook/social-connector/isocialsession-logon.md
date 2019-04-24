---
title: i、alsessionlogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: 指定したユーザー名とパスワードを使用して、ソーシャルネットワークサイトにログオンします。
ms.openlocfilehash: 7915097e456d6fafa713901f8074e6531bfaa001
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361041"
---
# <a name="isocialsessionlogon"></a>ISocialSession::Logon

指定したユーザー名とパスワードを使用して、ソーシャルネットワークサイトにログオンします。
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a>パラメーター

_<_
  
> 順番ログオンするユーザー名を含む文字列。
    
_password_
  
> 順番ログオンするパスワードを含む文字列。
    
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

