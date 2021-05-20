---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: userID パラメーターに基づいて ISocialPerson インターフェイスを取得します。
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439822"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

userID [パラメーターに基づいて ISocialPerson](isocialpersoniunknown.md) インターフェイス  _を取得_ します。 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>パラメーター

_userId_
  
> [in]ユーザーのユーザー ID または SMTP アドレスを含む文字列。
    
_result_
  
> [out] **ISocialPerson** インターフェイス。 
    
## <a name="remarks"></a>注釈

_userID パラメーターは_、ユーザー ID または SMTP アドレスである必要があります。 
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

