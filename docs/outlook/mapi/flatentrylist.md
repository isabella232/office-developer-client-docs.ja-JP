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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bc511ea4b3ec4eea9e38f744bcb8f277108085cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413858"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**適用対象**: Outlook 2013 | Outlook 2016 
  
[FLATENTRY 構造体の配列を含](flatentry.md)む。 
  
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
  
> abEntries **メンバーによって** 記述された配列内の **FLATENTRY 構造体の** 数。 
    
**cbEntries**
  
> abEntries で記述された配列内 **のバイト数** です。 
    
**abEntries**
  
> 端から端まで配置された 1 つ以上の **FLATENTRY** 構造体を含むバイト配列。 
    
## <a name="remarks"></a>注釈

**abEntries 配列では**、**各 FLATENTRY** 構造体は自然に整列された境界に配置されます。 余分なバイトは、2 つの FLATENTRY 構造体間の自然な配置を確実に行う埋 **め込みとして含** まれます。 配列内 **の最初の FLATENTRY** 構造体は **、abEntries** メンバーのオフセットが 8 なので、常に正しく配置されます。 次の構造体のオフセットを計算するには、4 の次の倍数に切り上げ、最初のエントリのサイズを使用します。 [CBFLATENTRY マクロを使用](cbflatentry.md)して **FLATENTRY 構造体のサイズを計算** します。 
  
たとえば、2 番目の **FLATENTRY** 構造体は、最初のエントリのオフセットと、次の 4 バイトに丸められた最初のエントリの長さで構成されるオフセットから始まります。 最初のエントリの長さは **、cb** メンバーの長さと **abEntry** メンバーの長さです。 
  
次のコード サンプルは **、FLATENTRYLIST 構造体のオフセットを計算する方法を示** しています。 _lpFlatEntry は、_ リスト内の最初の構造体へのポインターと仮定します。 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>関連項目

- [FLATENTRY](flatentry.md)
- [PidTagReplyRecipientEntries 標準プロパティ](pidtagreplyrecipiententries-canonical-property.md)
- [MAPI の構造](mapi-structures.md)

