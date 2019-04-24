---
title: i入力 alsessionfindperson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: userID パラメーターに一致する1人以上の人物を表す文字列を取得します。
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285372"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

_userID_パラメーターに一致する1人以上の人物を表す文字列を取得します。 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>パラメーター

_userId_
  
> 順番個人のソーシャルネットワークユーザー ID、SMTP アドレス、または表示名。
    
_result_
  
> 読み上げ_userId_パラメーターで指定された id 情報に一致する人物を表す XML 文字列。 
    
## <a name="remarks"></a>解説

1人以上の人物が**findperson**要求に一致した場合、このメソッドは_result_パラメーターでその人物の情報を返します。 _result_ XML 文字列は、Outlook Social Connector (.osc) プロバイダー拡張機能のスキーマで定義されているように、**フレンド**のスキーマ定義に準拠している必要があります。 
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

