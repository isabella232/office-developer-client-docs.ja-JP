---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: 空き時間情報データの指定された数のブロックをスキップします。
ms.openlocfilehash: baf13acb36d1455873771f1191461b7d17677959
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580413"
---
# <a name="ienumfbblockskip"></a>IEnumFBBlock::Skip

空き時間情報データの指定された数のブロックをスキップします。
  
## <a name="quick-info"></a>クイック ヒント

[「IEnumFBBlock」を参照](ienumfbblock.md)してください。
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a>パラメーター

_celt_
  
>  [in]スキップする空き時間情報ブロックの数。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="see-also"></a>関連項目

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)

