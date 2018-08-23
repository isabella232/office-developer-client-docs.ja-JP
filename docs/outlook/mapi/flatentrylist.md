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
ms.openlocfilehash: 371d0305f8f00e66704bae03f93857c7275b6a10
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589820"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**適用されます**: Outlook 2013 |Outlook 2016 
  
[FLATENTRY](flatentry.md)構造体の配列が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
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

**cEntries**
  
> **AbEntries**メンバーが記載されている配列内の**FLATENTRY**構造体の数です。 
    
**cbEntries**
  
> **AbEntries**で説明されている配列内のバイト数。 
    
**abEntries**
  
> バイト配列 1 つまたは複数の**FLATENTRY**構造体を含むエンド ・ ツー ・ エンド配置します。 
    
## <a name="remarks"></a>注釈

**AbEntries**アレイでは、各**FLATENTRY**構造体が揃えられた自然な境界に揃えられます。 余分なバイトは、確かに自然の配置の 2 つの**FLATENTRY**構造体の間に埋め込み文字として含まれます。 配列内の最初の**FLATENTRY**構造体は、 **abEntries**メンバーのオフセットが 8 であるために常に、正しく配置されます。 次の構造体のオフセットの計算には、最初のエントリのサイズを使用して、次に 4 の倍数に切り上げられます。 **FLATENTRY**構造体のサイズを計算するのにには、 [CbFLATENTRY](cbflatentry.md)マクロを使用します。 
  
などの 2 番目の**FLATENTRY**構造体は、最初のエントリのオフセットを加えた次の 4 バイトに丸められた最初のエントリの長さで構成されているオフセットから開始されます。 最初のエントリの長さは、 **abEntry**メンバーの長さを足したものを**cb**のメンバーの長さです。 
  
次のコード サンプルでは、 **FLATENTRYLIST**構造体のオフセットを計算する方法を示します。 その_lpFlatEntry_が、リスト内の最初の構造体へのポインターであることと仮定します。 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>関連項目

- [FLATENTRY](flatentry.md)
- [PidTagReplyRecipientEntries 標準プロパティ](pidtagreplyrecipiententries-canonical-property.md)
- [MAPI の構造](mapi-structures.md)

