---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: 列挙を指定した期間に制限します。
ms.openlocfilehash: 0dcb2cb2304323a4d434bb315531190f36e96e96
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596611"
---
# <a name="ienumfbblockrestrict"></a>IEnumFBBlock::Restrict

列挙を指定した期間に制限します。
  
## <a name="quick-info"></a>クイック ヒント

[「IEnumFBBlock」を参照](ienumfbblock.md)してください。
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a>パラメーター

_ftmStart_
  
>  [in]列挙を制限する開始時刻。 
    
_ftmEnd_
  
> [in]列挙を制限する終了時刻。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

また、このメソッドは列挙をリセットします。
  
## <a name="see-also"></a>関連項目

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)  
- [空き時間情報データにアクセスするのに相対時間を使用する](how-to-use-relative-time-to-access-free-busy-data.md)

