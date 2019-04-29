---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: 空き時間情報データの指定した数のブロックをスキップします。
ms.openlocfilehash: cf8ae18b5ed2c24a48d44d9e8d461da7d95054d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425723"
---
# <a name="ienumfbblockskip"></a>IEnumFBBlock::Skip

空き時間情報データの指定した数のブロックをスキップします。
  
## <a name="quick-info"></a>クイック ヒント

[IEnumFBBlock](ienumfbblock.md)を参照してください。
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a>パラメーター

_が大き_
  
>  順番スキップする空き時間ブロックの数。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="see-also"></a>関連項目

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)

