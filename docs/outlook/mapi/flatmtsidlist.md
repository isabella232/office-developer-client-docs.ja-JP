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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ea841ef4bc551581fb2d9ca90201b4615e67f134
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800075"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**適用されます**: Outlook 
  
それぞれの X.400 メッセージ転送システム (MTS) エントリ識別子が含まれています、 [MTSID](mtsid.md)構造体の配列が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
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

 **cMTSIDs**
  
> **MTSID**の構造体**abMTSIDs**のメンバーによって説明されている配列内の数です。 
    
 **cbMTSIDs**
  
> **AbMTSIDs**で説明されている配列内のバイト数。
    
 **abMTSIDs**
  
> **MTSID**の構造体 1 つまたは複数にはが含まれているバイト配列。 
    
## <a name="remarks"></a>備考

X.400 メッセージングの**FLATMTSIDLIST**構造体の使用は、MAPI メッセージの[FLATENTRYLIST](flatentrylist.md)構造体の使用に対応します。 MAPI は、メッセージの処理中に、X.400 のプロパティを維持するために**FLATMTSIDLIST**構造体を使用します。 サービス プロバイダーは、着信および発信 X.400 メッセージを処理する場合、 **FLATMTSIDLIST**構造体を使用します。 
  
**AbMTSIDs**アレイでは、 **MTSID**の各構造体が揃えられた自然な境界に揃えられます。 余分なバイトは、確かに自然の配置の 2 つの**MTSID**構造体の間に埋め込み文字として含まれます。 配列内の最初の**MTSID**構造体は、 **abMTSIDs**メンバーのオフセットが 8 であるために常に、正しく配置されます。 次の構造体のオフセットの計算には、最初のエントリのサイズを使用して、次に 4 の倍数に切り上げられます。 **MTSID**構造体のサイズを計算するのにには、 [CbNewMTSID](cbnewmtsid.md)マクロを使用します。 
  
## <a name="see-also"></a>関連項目



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[MAPI の構造](mapi-structures.md)

