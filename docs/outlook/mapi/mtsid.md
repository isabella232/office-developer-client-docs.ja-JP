---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96da91acec741322e6c07c64555171d35f0f7e00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342771"
---
# <a name="mtsid"></a>MTSID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
には、メッセージトランスポートシステム (MTS) エントリ id が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbMTSID](cbmtsid.md)、 [CbNewMTSID](cbnewmtsid.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a>Members

 **cb**
  
> **abentry**メンバーによって記述された配列内のバイト数。 
    
 **abentry**
  
> MTS エントリ識別子データを含むバイト配列。
    
## <a name="remarks"></a>解説

**MTSID**構造体は、MAPI エントリ識別子の X 400 マッピングに対してのみ使用されます。 MAPI の[FLATENTRY](flatentry.md)構造に対応しています。 
  
MTS 識別子の形式は、MAPI エントリ識別子またはバイナリプロパティの値と同じです。 MTS 識別子は、延期されたメッセージのキャンセルに特に役立ちます。 
  
## <a name="see-also"></a>関連項目



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[MAPI の構造](mapi-structures.md)

