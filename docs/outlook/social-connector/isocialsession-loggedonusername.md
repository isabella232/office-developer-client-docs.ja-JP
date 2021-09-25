---
title: ISocialSessionLoggedOnUserName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c0e7b788-3198-499c-ae21-b2032f929ed9
description: ログオン時に使用されるユーザー名を表す文字列を返します。
ms.openlocfilehash: 0155138551d777958ca0f4903bb3d24339a14d56
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563211"
---
# <a name="isocialsessionloggedonusername"></a>ISocialSession::LoggedOnUserName

ログオン時に使用されるユーザー名を表す文字列を返します。
  
```cpp
[propget] HRESULT _stdcall LoggedOnUserName([out, retval] BSTR* result);
```

## <a name="property-value"></a>プロパティ値

ログオンしているユーザーのユーザー名を表す文字列。
  
## <a name="see-also"></a>関連項目

- [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md)  
- [ISocialSession : IUnknown](isocialsessioniunknown.md)

