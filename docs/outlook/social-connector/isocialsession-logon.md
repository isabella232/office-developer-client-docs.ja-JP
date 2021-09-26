---
title: ISocialSessionLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: 指定したユーザー名とパスワードを使用してソーシャル ネットワーク サイトにログオンします。
ms.openlocfilehash: 03d37024f8c537d85134e9abc4ca6b0f6c097cf6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608827"
---
# <a name="isocialsessionlogon"></a>ISocialSession::Logon

指定したユーザー名とパスワードを使用してソーシャル ネットワーク サイトにログオンします。
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a>パラメーター

_ユーザー名_
  
> [in]ログオンするユーザー名を含む文字列。
    
_password_
  
> [in]ログオンするパスワードを含む文字列。
    
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

