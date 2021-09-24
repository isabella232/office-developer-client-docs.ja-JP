---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ebb7366dbbc49cfe38a95383f64b1195ef401fd9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550149"
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

## <a name="members"></a>メンバー

 **cValues**
  
> lpat メンバーが指す配列内の **値の** 数。 
    
 **lpat**
  
> アプリケーションの時刻値の配列へのポインター。 
    
## <a name="remarks"></a>注釈

**SAppTimeArray 構造体は**、データ型のプロパティを定義するために使用PT_MV_APPTIME。 プロパティの詳細については、「PT_MV_APPTIMEプロパティ [の種類の一覧」を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

