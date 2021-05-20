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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e9468d0c7fc7e46475afe19f12f225e53196639e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439402"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
データ型のプロパティを記述するために使用される通貨値の配列をPT_MV_CURRENCY。 
  
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

 **cValues**
  
> lpcur メンバーが指す配列内の **値の** 数。 
    
 **lpcur**
  
> 通貨値を含む [CURRENCY](currency.md) 構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

プロパティの詳細についてはPT_MV_CURRENCYプロパティ [の種類の一覧を参照してください](property-types.md)。 
  
## <a name="see-also"></a>関連項目



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

