---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: 列挙子内の指定した数のアカウントをスキップします。
ms.openlocfilehash: c8c7dbcf58b5e66de4291a489f8afd3a71474eca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617091"
---
# <a name="iolkenumskip"></a>IOlkEnum::Skip

列挙子内の指定した数のアカウントをスキップします。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkEnum」を参照してください](iolkenum.md)。
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a>パラメーター

_cSkip_
  
> [in]スキップするアカウントの数。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="see-also"></a>関連項目

- [IOlkEnum::GetCount](iolkenum-getcount.md) 
- [IOlkEnum::GetNext](iolkenum-getnext.md)  
- [IOlkEnum::Reset](iolkenum-reset.md)

