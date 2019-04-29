---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439703"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから構築されたダイアログボックスに表示される複数値リストを記述します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>メンバー

 **ulFlags**
  
> 予約語0である必要があります。
    
 **ulMVPropTag**
  
> PT_MV_TSTRING 型の複数値プロパティのプロパティタグ。
    
## <a name="remarks"></a>注釈

**DTBLMVLISTBOX**構造体には、アイテムの読み取り専用リストを持つ標準的な複数値リストが記述されています。 標準の複数値を持つリストを使用すると、値がすぐに表示されます。 
  
表示されるデータは、 **ulMVPropTag**メンバーで識別されるプロパティから取得されます。 表示テーブルに関連付けられているプロパティインターフェイスを読み取るための要件はありません。 また、ユーザーはこれらの種類のリストから選択することができないため、データはプロパティインターフェイスに書き込まれません。 
  
複数値のリストでは、複数値の文字列プロパティのみがサポートされています。その他の複数値プロパティの型はサポートされていません。 
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

