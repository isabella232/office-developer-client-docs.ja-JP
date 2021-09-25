---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: 同じ時間制限を使用して、列挙子のコピーを作成しますが、カーソルを列挙子の先頭に設定します。
ms.openlocfilehash: 248b65ccc493f574c8485d228c3e8f853df2a1fa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567999"
---
# <a name="ienumfbblockclone"></a>IEnumFBBlock::Clone

同じ時間制限を使用して、列挙子のコピーを作成しますが、カーソルを列挙子の先頭に設定します。
  
## <a name="quick-info"></a>クイック ヒント

[「IEnumFBBlock」を参照](ienumfbblock.md)してください。
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a>パラメーター

_ppclone_
  
> [out] [IEnumFBBlock](ienumfbblock.md) インターフェイスのコピーへのポインター。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_OUTOFMEMORY  <br/> |コピーを作成するメモリが不足しています。  <br/> |
   
## <a name="see-also"></a>関連項目

- [定数 (空き時間情報 API)](constants-free-busy-api.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

