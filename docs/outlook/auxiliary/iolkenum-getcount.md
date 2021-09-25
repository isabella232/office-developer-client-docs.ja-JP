---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: 列挙子内のアカウントの数を取得します。
ms.openlocfilehash: 5f5db79228791e3a9dc745f42560edb6901e8766
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551990"
---
# <a name="iolkenumgetcount"></a>IOlkEnum::GetCount

列挙子内のアカウントの数を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkEnum」を参照してください](iolkenum.md)。
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a>パラメーター

_pulCount_
  
> [out]列挙するオブジェクトの数を指すポインター。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="see-also"></a>関連項目

- [IOlkEnum::GetNext](iolkenum-getnext.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

