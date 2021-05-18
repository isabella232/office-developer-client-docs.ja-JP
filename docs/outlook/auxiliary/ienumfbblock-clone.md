---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: 同じ時間制限を使用して、列挙子のコピーを作成しますが、カーソルを列挙子の先頭に設定します。
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413403"
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

