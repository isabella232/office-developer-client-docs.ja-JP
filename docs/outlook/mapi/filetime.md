---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 00355546717ca61492750cb1dd113d20114b0695
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334812"
---
# <a name="filetime"></a>FILETIME

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ファイルの、未署名の64ビットの日付と時刻の値を保持します。 この値は、1601年1月1日からの100ナノ秒単位の数を表します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>Members

 **dwlowdatetime**
  
> file time 値の低順位32ビット。 
    
 **dwHighDateTime**
  
> file time 値の上位32ビット。
    
## <a name="remarks"></a>解説

PT_SYSTIME 型のプロパティには、その値の**FILETIME**構造があります。 このようなプロパティは、 [spropvalue](spropvalue.md)構造の定義において、**値**メンバーの**FILETIME**データ型を持っています。 
  
**FILETIME**構造体の定義は、 _Win32 プログラマーズリファレンス_および MAPI ヘッダーファイル mapidefs.h にあります。 MAPI は、Win32 定義が使用できない場合に、その構造が定義されていることを確認するために、その構造を定義します。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

