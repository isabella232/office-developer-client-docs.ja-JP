---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: ユーザー Id のパラメーターに基づいて、ISocialPerson インターフェイスを取得します。
ms.openlocfilehash: 5769f4c41bb97f45ab722f1b3a3febe24c8a7ab2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804362"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

_ユーザー Id_のパラメーターに基づいて、 [ISocialPerson](isocialpersoniunknown.md)インターフェイスを取得します。 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>パラメーター

_userId_
  
> [in]人のユーザー ID、または SMTP アドレスを含む文字列です。
    
_result_
  
> [out]**ISocialPerson**インターフェイスです。 
    
## <a name="remarks"></a>注釈

_ユーザー Id_パラメーターは、ユーザーの ID または SMTP アドレスである必要があります。 
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

