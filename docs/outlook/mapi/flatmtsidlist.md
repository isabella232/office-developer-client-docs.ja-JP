---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 207978d840272b52ce13422cae9172dd7045cbf7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576276"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[MTSID 構造体の配列を含](mtsid.md)み、それぞれ X.400 メッセージ トランスポート システム (MTS) エントリ識別子が含まれています。 
  
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
  
> **abMTSIDs** メンバーによって記述された配列内の **MTSID** 構造体の数。 
    
 **cbMTSIDs**
  
> **abMTSIDs** で記述された配列内のバイト数です。
    
 **abMTSIDs**
  
> 1 つ以上の **MTSID 構造体を含むバイト** 配列。 
    
## <a name="remarks"></a>注釈

X.400 メッセージングでの **FLATMTSIDLIST** 構造体の使用は、MAPI メッセージングでの [FLATENTRYLIST](flatentrylist.md) 構造体の使用に対応します。 MAPI では **、FLATMTSIDLIST** 構造体を使用して、メッセージの処理中に X.400 プロパティを維持します。 サービス プロバイダーは、受信メッセージと送信 X.400 メッセージを処理するときに **FLATMTSIDLIST** 構造体を使用します。 
  
**abMTSIDs 配列では**、**各 MTSID** 構造体は自然に整列された境界に配置されます。 余分なバイトは、任意の 2 つの MTSID 構造体間の自然な配置を確認するために埋め **込みとして含** まれます。 配列内 **の最初の MTSID** 構造体は **、abMTSIDs** メンバーのオフセットが 8 なので、常に正しく配置されます。 次の構造体のオフセットを計算するには、4 の次の倍数に切り上げ、最初のエントリのサイズを使用します。 [CbNewMTSID マクロを使用](cbnewmtsid.md)して **、MTSID** 構造のサイズを計算します。 
  
## <a name="see-also"></a>関連項目



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[MAPI の構造](mapi-structures.md)

