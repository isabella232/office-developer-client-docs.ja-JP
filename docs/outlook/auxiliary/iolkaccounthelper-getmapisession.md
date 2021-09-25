---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: MAPI セッションを開き、アカウント マネージャーのセッションへの参照を維持します。
ms.openlocfilehash: 460317b5b83c3d2ef6aca26260d797502f7ea084
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617126"
---
# <a name="iolkaccounthelpergetmapisession"></a>IOlkAccountHelper::GetMapiSession

MAPI セッションを開き、アカウント マネージャーのセッションへの参照を維持します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccountHelper」を参照してください](iolkaccounthelper.md)。
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a>パラメーター

_ppmsess_
  
> [out]現在の MAPI セッション。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

循環参照の問題のため、アカウント マネージャー自体は MAPI セッションの参照を維持できません。
  
## <a name="see-also"></a>関連項目

- [IOlkAccountHelper::HandsOffSession](iolkaccounthelper-handsoffsession.md)
- [IMAPISession: IUnknown](https://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

