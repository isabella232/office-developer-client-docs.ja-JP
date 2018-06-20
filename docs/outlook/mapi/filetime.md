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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a5f950907e2b14cb4101a094715c24b25beb2016
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800063"
---
# <a name="filetime"></a>FILETIME

  
  
**適用されます**: Outlook 
  
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

## <a name="members"></a>メンバー

 **dwLowDateTime**
  
> ファイル時刻の値の下位 32 ビットです。 
    
 **dwHighDateTime**
  
> ファイル時刻の値の上位の 32 ビットです。
    
## <a name="remarks"></a>備考

タイプ PT_SYSTIME のプロパティは、 **FILETIME**構造体の値を持ちます。 このようなプロパティでは、**値**メンバー [SPropValue](spropvalue.md)構造体の定義内の**FILETIME**データ型があります。 
  
**FILETIME**構造体の定義は、 _Win32 プログラマーズ リファレンス_では、MAPI のヘッダー ファイル Mapidefs.h には。 MAPI では、Win32 の定義が使用可能な場合が定義されているかどうかを確認するには、条件付きで構造体を定義します。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

