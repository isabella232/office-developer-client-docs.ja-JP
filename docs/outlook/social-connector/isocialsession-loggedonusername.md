---
title: ISocialSessionLoggedOnUserName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c0e7b788-3198-499c-ae21-b2032f929ed9
description: ログオン時に使用されるユーザー名を表す文字列を返します。
ms.openlocfilehash: 6f0d2c68b1af9e7c96f2cd86dc798518e432c7cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285307"
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

