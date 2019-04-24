---
title: i、alsessiongetlogonurl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: web 認証中にブラウザーベースのフォームをユーザーに提示するために使用される URL を表す文字列を取得します。
ms.openlocfilehash: 83867282922ea136b9673609cc2ba2f1a206f6ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285379"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

web 認証中にブラウザーベースのフォームをユーザーに提示するために使用される URL を表す文字列を取得します。
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>パラメーター

_url_
  
> 読み上げweb 認証で使用するフォームの URL を含む文字列。
    
## <a name="remarks"></a>解説

フォームがユーザーに表示された後、i渡された[alsession:: logonweb](isocialsession-logonweb.md)メソッドが、ユーザーに空の__ 文字列を指定して呼び出されます。 
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

