---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 814cfeab61854469f460cc38f927b0e3723f6f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803926"
---
# <a name="sizedentryid"></a>SizedENTRYID

**適用されます**: Outlook 
  
指定したサイズの**ab**のメンバーを含む名前付き[エントリ ID](entryid.md)構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**エントリ ID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Parameters

__cb_
  
> **Ab**の新しい構造体のメンバーのバイト数をカウントします。 
    
__名_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>備考

**SizedENTRYID**マクロを使用して、配列の長さの要件を認識した後に、エントリの識別子を定義できます。 明示的な境界を持つエントリ識別子を作成するのにには、このマクロを使用します。 
  
**エントリ ID**の構造体へのポインターとしての**SizedENTRYID**マクロから得られる新しい構造体を使用するには、次のキャストを実行します。 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>関連項目

- [エントリ ID](entryid.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

