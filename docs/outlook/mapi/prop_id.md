---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 228ea91969b35a1608dd6b3378b751312aa9c665
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409133"
---
# <a name="prop_id"></a>PROP_ID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したプロパティ タグのプロパティ識別子を返します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a>パラメーター

 _ulPropTag_
  
> 返される識別子を含むプロパティ タグ。
    
## <a name="remarks"></a>注釈

すべてのプロパティ タグには、低次ワード (ビット 0 ~ 15) のプロパティ型と、高次ワード (ビット 16 ~ 31) のプロパティ識別子が含まれる。 この **PROP_ID** は、プロパティ識別子を抽出し、返される整数のビット 0 ~ 15 に格納します。 戻り値の残りのビットは 0 に設定されます。 
  
たとえば **PROP_ID** マクロを使用して [、IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)に渡す識別子を取得できます。 **GetNamesFromIDs は** 、名前付きプロパティの識別子に関連付けられたプロパティ名を取得します。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[構造に関連するマクロ](macros-related-to-structures.md)

