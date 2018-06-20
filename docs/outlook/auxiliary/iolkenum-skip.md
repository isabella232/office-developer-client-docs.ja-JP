---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: 列挙子内のアカウントの指定した数をスキップします。
ms.openlocfilehash: 2791f1204cedf5e91d13923e50dfc45b981b7e26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799486"
---
# <a name="iolkenumskip"></a>IOlkEnum::Skip

列挙子内のアカウントの指定した数をスキップします。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkEnum](iolkenum.md)を参照してください。
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a>Parameters

_cSkip_
  
> [in]スキップするアカウントの数です。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="see-also"></a>関連項目

- [IOlkEnum::GetCount](iolkenum-getcount.md) 
- [IOlkEnum::GetNext](iolkenum-getnext.md)  
- [IOlkEnum::Reset](iolkenum-reset.md)

