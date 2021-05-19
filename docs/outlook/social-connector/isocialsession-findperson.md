---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: userID パラメーターに一致する 1 人または複数のユーザーを表す文字列を取得します。
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434796"
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

