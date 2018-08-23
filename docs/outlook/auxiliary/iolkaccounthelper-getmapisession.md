---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: MAPI セッションを開くし、アカウント マネージャーのセッションへの参照を保持します。
ms.openlocfilehash: 50809a00d13fd9f2a93bebc2961a134b3625e82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799483"
---
# <a name="iolkaccounthelpergetmapisession"></a>IOlkAccountHelper::GetMapiSession

MAPI セッションを開くし、アカウント マネージャーのセッションへの参照を保持します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccountHelper](iolkaccounthelper.md)を参照してください。
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a>パラメーター

_ppmsess_
  
> [out]現在の MAPI セッションです。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解釈

循環参照の問題があるため、アカウント マネージャー自体は MAPI セッションの参照を維持できません。
  
## <a name="see-also"></a>関連項目

- [IOlkAccountHelper::HandsOffSession](iolkaccounthelper-handsoffsession.md)
- [IMAPISession: IUnknown](http://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

