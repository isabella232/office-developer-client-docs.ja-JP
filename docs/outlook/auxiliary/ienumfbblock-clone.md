---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: 同じ時間制限を使用していますが、列挙子の先頭にカーソルを設定する、列挙子のコピーを作成します。
ms.openlocfilehash: 51503be2091fa01da6f636bf6944274068617f05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799328"
---
# <a name="ienumfbblockclone"></a>IEnumFBBlock::Clone

同じ時間制限を使用していますが、列挙子の先頭にカーソルを設定する、列挙子のコピーを作成します。
  
## <a name="quick-info"></a>クイック ヒント

[IEnumFBBlock](ienumfbblock.md)を参照してください。
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a>Parameters

_ppclone_
  
> [out]A [IEnumFBBlock](ienumfbblock.md)インターフェイスのコピーへのポインターへのポインターがあります。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_OUTOFMEMORY  <br/> |コピーを作成するためのメモリが不足があります。  <br/> |
   
## <a name="see-also"></a>関連項目

- [定数 (空き時間情報の API)](constants-free-busy-api.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

