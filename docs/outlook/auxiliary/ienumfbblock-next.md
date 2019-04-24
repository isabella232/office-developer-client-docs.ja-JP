---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: 列挙で、次に指定された空き時間情報データのブロック数を取得します。
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319594"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

列挙で、次に指定された空き時間情報データのブロック数を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[IEnumFBBlock](ienumfbblock.md)を参照してください。
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a>パラメーター

_が大き_
  
> 順番取得する*pblk*内の空き時間情報のデータブロックの数。 
    
_pblk_
  
> 順番空き時間ブロックの配列へのポインター。 配列のサイズは、1に** 割り当てられます。 この配列には、要求された空き時間ブロックが返されます。 
    
_pcfetch_
  
> 読み上げ実際に*pblk*で返される空き時間ブロックの数。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |要求されたブロック数が返されました。  <br/> |
|S_FALSE  <br/> |要求されたブロック数が返されていません。  <br/> |
   
## <a name="see-also"></a>関連項目

- [定数 (空き時間情報 API)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

