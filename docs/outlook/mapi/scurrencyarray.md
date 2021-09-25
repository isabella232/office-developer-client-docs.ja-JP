---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 37847a0c2d5f4dcea96e7b3a7af6094e94a78791
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586755"
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

## <a name="members"></a>メンバー

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

