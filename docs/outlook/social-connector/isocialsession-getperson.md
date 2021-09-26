---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: userID パラメーターに基づいて ISocialPerson インターフェイスを取得します。
ms.openlocfilehash: 7546232b4ea758331dfd2ff5f794a0d14cafd590
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608826"
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

