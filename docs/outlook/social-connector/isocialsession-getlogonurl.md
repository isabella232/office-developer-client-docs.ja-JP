---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Web 認証時にユーザーにブラウザー ベースのフォームを表示するために使用される URL を表す文字列を取得します。
ms.openlocfilehash: 343919f194b238fc519bb8f6d808b44a8ab6e7b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804359"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Web 認証時にユーザーにブラウザー ベースのフォームを表示するために使用される URL を表す文字列を取得します。
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>Parameters

_url_
  
> [out]Web 認証で使用するフォームの URL を含む文字列です。
    
## <a name="remarks"></a>備考

フォームは、ユーザーに提示された後は、 _connectIn_パラメーターに空の文字列で[ISocialSession::LogonWeb](isocialsession-logonweb.md)メソッドが呼び出されます。 
  
## <a name="see-also"></a>関連項目

- [ISocialSession: IUnknown](isocialsessioniunknown.md)

