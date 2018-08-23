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
ms.openlocfilehash: d58a216a41ff8fe93387ce6d9d1d6aa16f36f224
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583254"
---
# <a name="filetime"></a>FILETIME

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
符号なし 64 ビットの日付と、ファイルの時刻の値を保持します。 この値は、1601 年 1 月 1 日の開始以降の 100 ナノ秒単位の数を表します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>Members

 **dwLowDateTime**
  
> ファイル時刻の値の下位 32 ビットです。 
    
 **dwHighDateTime**
  
> ファイル時刻の値の上位の 32 ビットです。
    
## <a name="remarks"></a>注釈

タイプ PT_SYSTIME のプロパティは、 **FILETIME**構造体の値を持ちます。 このようなプロパティでは、**値**メンバー [SPropValue](spropvalue.md)構造体の定義内の**FILETIME**データ型があります。 
  
**FILETIME**構造体の定義は、 _Win32 プログラマーズ リファレンス_では、MAPI のヘッダー ファイル Mapidefs.h には。 MAPI では、Win32 の定義が使用可能な場合が定義されているかどうかを確認するには、条件付きで構造体を定義します。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

