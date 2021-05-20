---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430386"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
時間値の配列を含む。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> lpat メンバーが指す配列内の **値の** 数。 
    
 **lpat**
  
> アプリケーションの時刻値の配列へのポインター。 
    
## <a name="remarks"></a>注釈

**SAppTimeArray 構造体は**、データ型のプロパティを定義するために使用PT_MV_APPTIME。 プロパティの詳細については、「PT_MV_APPTIMEプロパティ [の種類の一覧」を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

