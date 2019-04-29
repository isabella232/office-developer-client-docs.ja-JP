---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439220"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
には、 [MTSID](mtsid.md)構造体の配列が格納されています。それぞれには、1つのメッセージトランスポートシステム (MTS) エントリ識別子が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbFLATMTSIDLIST](cbflatmtsidlist.md)、 [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a>メンバー

 **cmtsids**
  
> **abmtsids**メンバーによって記述された、配列内の**MTSID**構造体の数。 
    
 **cbmtsids**
  
> **abmtsids**で記述された配列のバイト数。
    
 **abmtsids**
  
> 1つまたは複数の**MTSID**構造体を含むバイト配列。 
    
## <a name="remarks"></a>注釈

**FLATMTSIDLIST**におけるこの構造体の使用は、MAPI メッセージングでの[FLATENTRYLIST](flatentrylist.md)構造の使用に対応しています。 MAPI では、 **FLATMTSIDLIST**構造を使用して、メッセージ処理時に x. プロパティを維持します。 サービスプロバイダーは、受信および送信の X. 400 メッセージを処理するときに、 **FLATMTSIDLIST**構造体を使用します。 
  
**abmtsids**配列では、各**MTSID**構造は、自然に配置された境界に沿って配置されます。 2つの**MTSID**構造体間で自然な配置が行われるように、パディングとして追加のバイトが含まれています。 **abmtsids**メンバのオフセットは8であるため、配列内の最初の**MTSID**構造体は常に正確に調整されます。 次の構造体のオフセットを計算するには、最初のエントリのサイズを、次の4つの倍数まで切り上げて使用します。 [CbNewMTSID](cbnewmtsid.md)マクロを使用して、 **MTSID**構造体のサイズを計算します。 
  
## <a name="see-also"></a>関連項目



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[MAPI の構造](mapi-structures.md)

