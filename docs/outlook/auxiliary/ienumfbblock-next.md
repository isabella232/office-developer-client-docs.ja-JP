---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: 列挙の空き時間情報データの次に指定したブロック数を取得します。
ms.openlocfilehash: b1ebf09aaca466fdd6ee9fc3017d6b395d4326ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605429"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

列挙の空き時間情報データの次に指定したブロック数を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[「IEnumFBBlock」を参照](ienumfbblock.md)してください。
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a>パラメーター

_celt_
  
> [in]取得する pblk 内の空き時間  *情報データ ブロックの*  数。 
    
_pblk_
  
> [in]空き時間情報ブロックの配列へのポインター。 配列には、celt のサイズが  *割り当てられている*  。 要求された空き時間情報ブロックは、この配列で返されます。 
    
_pcfetch_
  
> [out]pblk で実際に返される空き時間情報ブロック  *の数*  です。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |要求されたブロック数が返されました。  <br/> |
|S_FALSE  <br/> |要求されたブロック数は返されません。  <br/> |
   
## <a name="see-also"></a>関連項目

- [定数 (空き時間情報 API)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

