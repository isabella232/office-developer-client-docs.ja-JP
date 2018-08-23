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
ms.openlocfilehash: e42bbf23ea8cf4e6196017a962329366e168420d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801665"
---
# <a name="mtsid"></a>MTSID

  
  
**適用対象**: Outlook 
  
X.400 メッセージ転送システム (MTS) エントリ識別子が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
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
  
> **AbEntry**メンバーが記載されている配列内のバイト数。 
    
 **abEntry**
  
> MTS のエントリの識別子のデータを格納するバイトの配列です。
    
## <a name="remarks"></a>注釈

**MTSID**構造体は、MAPI エントリの識別子の X.400 マッピングに対してのみ使用されます。 MAPI [FLATENTRY](flatentry.md)構造体に対応します。 
  
MTS 識別子には、MAPI エントリの識別子またはバイナリのプロパティ値と同じ形式があります。 MTS 識別子は遅延メッセージをキャンセルするときに便利にすることはできます。 
  
## <a name="see-also"></a>関連項目



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[MAPI の構造](mapi-structures.md)

