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
ms.openlocfilehash: e1846b4be93bf6300ea89a9ae3133fbba82b344e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573125"
---
# <a name="propid"></a>PROP_ID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
指定されたプロパティ タグのプロパティの識別子を返します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a>パラメーター

 _ulPropTag_
  
> 返される識別子を格納するプロパティ タグです。
    
## <a name="remarks"></a>注釈

プロパティのすべてのタグには、下位ワード (ビット 0 ~ 15) のプロパティの型と、上位ワード (16 ~ 31 のビット) のプロパティの識別子が含まれています。 **PROP_ID**マクロは、プロパティの識別子を抽出し返される整数の 15 からビット 0 に入れます。 戻り値の残りのビットは、0 に設定されます。 
  
たとえば、 **PROP_ID**マクロは、 [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)に渡すための識別子を取得する場合に使用できます。 **GetNamesFromIDs**は、名前付きプロパティの識別子に関連付けられているプロパティ名を取得します。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[構造体に関連するマクロ](macros-related-to-structures.md)

