---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fd1f8d3f62893586f7ca3c06459a0dee149ea055
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601094"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから作成されたダイアログ ボックスに表示される複数値のリストについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>メンバー

 **ulFlags**
  
> 予約済み。は 0 である必要があります。
    
 **ulMVPropTag**
  
> 型の複数値プロパティのプロパティ タグPT_MV_TSTRING。
    
## <a name="remarks"></a>注釈

**DTBLMVLISTBOX** 構造体は、アイテムの読み取り専用リストを持つ標準の複数値リストを記述します。 標準の複数値リストを使用すると、値はすぐに表示されます。 
  
表示されるデータは **、ulMVPropTag** メンバーで識別されるプロパティから取得されます。 表示テーブルに関連付けられているプロパティ インターフェイスから読み取る必要はありません。 また、ユーザーはこれらの種類のリストから選択を行えないので、データはプロパティ インターフェイスに書き込まれます。 
  
複数値のリストでは、複数値の文字列プロパティだけがサポートされます。他の複数値プロパティの種類はサポートされていません。 
  
表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。 表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

