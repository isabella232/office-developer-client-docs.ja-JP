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
  
PT_MV_CURRENCY 型のプロパティを記述するために使用される通貨値の配列を格納します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a>メンバー

 **cvalues**
  
> lpcur メンバーによって参照されて**** いる配列内の値の数。 
    
 **lpcur**
  
> 通貨の値を含む[通貨](currency.md)構造の配列へのポインター。 
    
## <a name="remarks"></a>注釈

PT_MV_CURRENCY の詳細については、「[プロパティの種類の一覧](property-types.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

