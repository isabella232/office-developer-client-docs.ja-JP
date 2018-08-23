---
title: ISocialSessionLoggedOnUserID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54377ab4-8c69-4d7a-b9b7-278241823c8d
description: 現在ログオンしているユーザーのソーシャル ネットワークのユーザー ID を表す文字列を返します。
ms.openlocfilehash: dcc81d7acf8a839e7fe3249cc0eb06f96c113b56
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804365"
---
# <a name="isocialsessionloggedonuserid"></a>ISocialSession::LoggedOnUserID

現在ログオンしているユーザーのソーシャル ネットワークのユーザー ID を表す文字列を返します。 
  
```cpp
[propget] HRESULT _stdcall LoggedOnUserID([out, retval] BSTR* result);
```

## <a name="property-value"></a>プロパティ値

ログオンしたユーザーのソーシャル ネットワークのユーザー ID を含む文字列です。
  
## <a name="see-also"></a>関連項目

- [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md)  
- [ISocialSession : IUnknown](isocialsessioniunknown.md)

