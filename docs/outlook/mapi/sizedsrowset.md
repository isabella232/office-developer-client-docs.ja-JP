---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8b7a93a9abb9a1c589ac7fdab3723c9c924eea0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803929"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**適用されます**: Outlook 
  
指定された行数を格納する名前付き[SRowSet](srowset.md)構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Parameters

__クロウズ_
  
> 新しい構造体に含まれる行の数のカウントです。
    
__名_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>備考

**SRowSet**構造体へのポインターとしての**SizedSRowSet**マクロから得られる新しい構造体を使用するには、次のキャストを実行します。 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>関連項目

- [SRowSet](srowset.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

