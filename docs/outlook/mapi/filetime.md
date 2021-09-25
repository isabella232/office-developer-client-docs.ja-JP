---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ac1a9a4b84e50e1e979a3228d30067877f20eef5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614207"
---
# <a name="filetime"></a>FILETIME

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ファイルの符号なし 64 ビットの日付と時刻の値を保持します。 この値は、1601 年 1 月 1 日の開始以降の 100 ナノ秒単位の数を表します。 
  
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

## <a name="members"></a>メンバー

 **dwLowDateTime**
  
> ファイル時間値の低次 32 ビット。 
    
 **dwHighDateTime**
  
> ファイル時間値の高次 32 ビット。
    
## <a name="remarks"></a>注釈

型のプロパティはPT_SYSTIME **の FILETIME** 構造を持っています。 このようなプロパティには **、SPropValue** 構造体の定義内の **Value** メンバーの [FILETIME](spropvalue.md) データ型があります。 
  
FILETIME 構造 **の定義** は  _、Win32 プログラマ_ リファレンスと MAPI ヘッダー ファイル Mapidefs.h に含まれています。 MAPI は、Win32 定義が使用できないときに定義されるように条件付きで構造を定義します。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

