---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: userID パラメーターに一致する 1 人または複数のユーザーを表す文字列を取得します。
ms.openlocfilehash: 789f98dcc8e4b09a230d148644f60a2fbf1c3328
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594917"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

userID パラメーターに一致する 1 人または複数のユーザーを表す  _文字列を取得_ します。 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>パラメーター

_userId_
  
> [in]ソーシャル ネットワーク のユーザー ID、SMTP アドレス、またはユーザーの表示名。
    
_result_
  
> [out]  _userId_ パラメーターで指定された識別情報に一致する 1 人または複数のユーザーを表す XML 文字列。 
    
## <a name="remarks"></a>注釈

1 人または複数のユーザーが **FindPerson** 要求と一致する場合、このメソッドは result パラメーター内のそれらのユーザーの情報を  _返_ します。 結果 _の_ XML 文字列は、ソーシャル コネクタ(OSC) プロバイダーの機能拡張のスキーマで定義されているフレンドのスキーマ定義Outlook準拠している必要があります。 
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

