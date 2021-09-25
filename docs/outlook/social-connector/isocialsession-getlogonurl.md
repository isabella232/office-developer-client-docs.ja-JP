---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Web 認証中にブラウザー ベースのフォームをユーザーに表示するために使用される URL を表す文字列を取得します。
ms.openlocfilehash: eeb822c40541ffb46fb8ac3087aa7bef21601d04
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590395"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Web 認証中にブラウザー ベースのフォームをユーザーに表示するために使用される URL を表す文字列を取得します。
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>パラメーター

_url_
  
> [out]Web 認証で使用されるフォームの URL を含む文字列。
    
## <a name="remarks"></a>注釈

フォームがユーザーに提示された後 [、iSocialSession::LogonWeb](isocialsession-logonweb.md) メソッドは  _、connectIn_ パラメーターの空の文字列で呼び出されます。 
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

