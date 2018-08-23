---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c440bb7d8f3d2d3002a4d1a80ca3a671b49f4d2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803851"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**適用対象**: Outlook 
  
PT_MV_CURRENCY の種類のプロパティを説明するために使用する通貨値の配列が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a>Members

 **あう**
  
> **Lpcur**メンバーが指す配列内の値の数です。 
    
 **lpcur**
  
> 通貨値が含まれている[通貨](currency.md)の構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

PT_MV_CURRENCY については、[プロパティの種類の一覧](property-types.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

