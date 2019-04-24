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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 228ea91969b35a1608dd6b3378b751312aa9c665
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328575"
---
# <a name="propid"></a>PROP_ID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したプロパティタグのプロパティ識別子を返します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a>パラメーター

 _ulPropTag_
  
> 返される識別子を含む Property タグ。
    
## <a name="remarks"></a>解説

すべてのプロパティタグには、下位ワード (ビット 0 ~ 15) のプロパティの種類と、上位ワード (ビット 16 ~ 31) のプロパティの識別子が含まれています。 **PROP_ID**マクロは、プロパティ識別子を抽出し、それをビット 0 ~ 15 の整数に格納して返します。 戻り値の残りのビットは0に設定されます。 
  
**PROP_ID**マクロは、たとえば、 [imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)に渡す識別子を取得するために使用できます。 **GetNamesFromIDs**は、名前付きプロパティの識別子に関連付けられたプロパティ名を取得します。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[構造に関連するマクロ](macros-related-to-structures.md)

