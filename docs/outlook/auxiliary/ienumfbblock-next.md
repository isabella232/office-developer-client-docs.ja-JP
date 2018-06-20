---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: 列挙型の中の空き時間情報データ ブロックの次の指定された番号を取得します。
ms.openlocfilehash: ec366cf102d3c75487f9485cfae7764d68695f10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799334"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

列挙型の中の空き時間情報データ ブロックの次の指定された番号を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[IEnumFBBlock](ienumfbblock.md)を参照してください。
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a>Parameters

_celt_
  
> [in]*Pblk*を取得するには、空き時間情報データの数がブロックされます。 
    
_pblk_
  
> [in]空き時間ブロックの配列へのポインター。 配列は、 *celt*のサイズが割り当てられます。 要求された空き時間情報のブロックは、この配列で返されます。 
    
_pcfetch_
  
> [out]*Pblk*に実際に返される空き時間情報のブロックの数。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |要求されたブロックの数が返されました。  <br/> |
|S_FALSE  <br/> |要求されたブロックの数が取得できませんでした。  <br/> |
   
## <a name="see-also"></a>関連項目

- [定数 (空き時間情報の API)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

