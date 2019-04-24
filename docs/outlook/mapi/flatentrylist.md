---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bc511ea4b3ec4eea9e38f744bcb8f277108085cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336898"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**適用対象**: Outlook 2013 | Outlook 2016 
  
[FLATENTRY](flatentry.md)構造体の配列を格納します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbFLATENTRYLIST](cbflatentrylist.md)、 [CbNewFLATENTRYLIST](cbnewflatentrylist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a>Members

**centries**
  
> **abentries**メンバーによって記述された、配列内の**FLATENTRY**構造体の数。 
    
**cbentries**
  
> **abentries**で記述された配列内のバイト数。 
    
**abentries**
  
> 1つまたは複数の**FLATENTRY**構造を含むバイト配列。エンドツーエンドで配置されています。 
    
## <a name="remarks"></a>解説

**abentries**配列では、各**FLATENTRY**構造は、自然に配置された境界に沿って配置されます。 2つの**FLATENTRY**構造体間で自然な配置が行われるように、パディングとして追加のバイトが含まれています。 **abentries**メンバーのオフセットは8であるため、配列内の最初の**FLATENTRY**構造体は常に正確に調整されます。 次の構造体のオフセットを計算するには、最初のエントリのサイズを、次の4つの倍数まで切り上げて使用します。 [CbFLATENTRY](cbflatentry.md)マクロを使用して、 **FLATENTRY**構造体のサイズを計算します。 
  
たとえば、2番目の**FLATENTRY**構造体は、最初のエントリのオフセットと、次の4バイトに丸められた最初のエントリの長さで構成されるオフセットから始まります。 最初のエントリの長さは、 **cb**メンバーの長さに**abentry**メンバーの長さを加えたものです。 
  
次のコードサンプルは、 **FLATENTRYLIST**構造体でオフセットを計算する方法を示しています。 _lpFlatEntry_はリスト内の最初の構造体へのポインターであると仮定します。 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>関連項目

- [FLATENTRY](flatentry.md)
- [PidTagReplyRecipientEntries 標準プロパティ](pidtagreplyrecipiententries-canonical-property.md)
- [MAPI の構造](mapi-structures.md)

