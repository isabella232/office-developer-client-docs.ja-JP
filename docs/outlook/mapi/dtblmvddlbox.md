---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 384282445e6f50fac3d440e4df3a4c8e61e0c8a8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551668"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから作成されたダイアログ ボックスで使用されるドロップダウン リストについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a>メンバー

 **ulFlags**
  
> 予約済み。は 0 である必要があります。
    
 **ulMVPropTag**
  
> 型の複数値プロパティのプロパティ タグPT_MV_TSTRING。 このプロパティの異なる値は、ドロップダウン リストに個別のエントリとして表示されます。
    
## <a name="remarks"></a>注釈

**DTBLMVDDLBOX** 構造体は、複数値のドロップダウン リストを項目の読み取り専用リストとして記述します。 複数値のドロップダウン リストを使用すると、ユーザーがスクロール バーをクリックすると値が表示されます。 
  
表示されるデータは **、ulMVPropTag** メンバーで識別されるプロパティから取得されます。 表示テーブルに関連付けられているプロパティ インターフェイスから読み取る必要はありません。 また、ユーザーはこのような種類のリスト ボックスから選択を行えないので、データはプロパティ インターフェイスに書き込まれます。 
  
複数値のドロップダウン リストでは、複数値の文字列プロパティだけがサポートされます。他の複数値プロパティの種類はサポートされていません。 
  
表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。 表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

