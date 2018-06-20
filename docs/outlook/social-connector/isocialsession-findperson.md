---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: ユーザー Id パラメーターに一致する 1 つまたは複数の人物を表す文字列を取得します。
ms.openlocfilehash: 0b7525f853f7d97a991e2996a4e715cc53756d4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804360"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

_ユーザー Id_パラメーターに一致する 1 つまたは複数の人物を表す文字列を取得します。 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameters

_userId_
  
> [in]ソーシャル ネットワークのユーザー ID では、SMTP アドレス、またはユーザーの名前を表示します。
    
_result_
  
> [out]_ユーザー Id_パラメーターで指定された識別情報に一致する 1 つまたは複数の担当者を表す XML 文字列です。 
    
## <a name="remarks"></a>備考

1 つまたは複数の担当者には、 **FindPerson**要求が一致すると、このメソッドは、_結果_のパラメーターにしている人の情報を返します。 _結果_の XML 文字列は、Outlook ソーシャル コネクタ (OSC) プロバイダーの機能拡張のスキーマで定義されている**友人**のスキーマ定義に従う必要があります。 
  
## <a name="see-also"></a>関連項目

- [ISocialSession: IUnknown](isocialsessioniunknown.md)

