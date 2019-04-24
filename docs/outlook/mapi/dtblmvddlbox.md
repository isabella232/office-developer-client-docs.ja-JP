---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 33b4fd87f33c26db15e1a6a28f077c393168db91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325761"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから構築されたダイアログボックスで使用されるドロップダウンリストを表します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a>メンバー

 **ulFlags**
  
> 予約語0である必要があります。
    
 **ulMVPropTag**
  
> PT_MV_TSTRING 型の複数値プロパティのプロパティタグ。 このプロパティの異なる値は、ドロップダウンリストに個別のエントリとして表示されます。
    
## <a name="remarks"></a>解説

**DTBLMVDDLBOX**構造体は、複数値を持つドロップダウンリストに、アイテムの読み取り専用リストを記述します。 複数値を持つドロップダウンリストを使用すると、ユーザーがスクロールバーをクリックしたときに値が表示されます。 
  
表示されるデータは、 **ulMVPropTag**メンバーで識別されるプロパティから取得されます。 表示テーブルに関連付けられているプロパティインターフェイスを読み取るための要件はありません。 また、ユーザーはこれらの種類のリストボックスから選択することができないため、データはプロパティインターフェイスに書き込まれません。 
  
複数値のドロップダウンリストでは、複数値の文字列プロパティのみがサポートされています。その他の複数値プロパティの型はサポートされていません。 
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

