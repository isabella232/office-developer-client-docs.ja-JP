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
ms.openlocfilehash: 59e9cf23aed2a389384318468c3853cd41c9ec1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585683"
---
# <a name="mtsid"></a>MTSID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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

