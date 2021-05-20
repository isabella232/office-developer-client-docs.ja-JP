---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Web 認証中にブラウザー ベースのフォームをユーザーに表示するために使用される URL を表す文字列を取得します。
ms.openlocfilehash: 83867282922ea136b9673609cc2ba2f1a206f6ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427914"
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

