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
ms.openlocfilehash: 02485ad2a510a81c64406ea6ec9a0f85c0e4d2f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804487"
---
# <a name="isocialsessionloggedonusername"></a>ISocialSession::LoggedOnUserName

ログオン時に使用されるユーザー名を表す文字列を返します。
  
```cpp
[propget] HRESULT _stdcall LoggedOnUserName([out, retval] BSTR* result);
```

## <a name="property-value"></a>プロパティ値

ログオン ユーザーのユーザー名を表す文字列。
  
## <a name="see-also"></a>関連項目

- [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md)  
- [ISocialSession : IUnknown](isocialsessioniunknown.md)

