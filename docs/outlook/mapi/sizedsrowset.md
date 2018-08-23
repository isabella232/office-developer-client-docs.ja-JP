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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b8c70c8b13025f196fdebb2956939bec840a96f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583940"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**適用されます**: Outlook 2013 |Outlook 2016 
  
指定された行数を格納する名前付き[SRowSet](srowset.md)構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>パラメーター

__クロウズ_
  
> 新しい構造体に含まれる行の数のカウントです。
    
__名_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>注釈

**SRowSet**構造体へのポインターとしての**SizedSRowSet**マクロから得られる新しい構造体を使用するには、次のキャストを実行します。 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>関連項目

- [SRowSet](srowset.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

