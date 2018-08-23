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
ms.openlocfilehash: ede0a448a32565446e614fc2d14f2a72a9549dad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799990"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**適用対象**: Outlook 
  
ディスプレイ テーブルから組み込まれているダイアログ ボックスで使用するボックスの一覧について説明します。
  
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

## <a name="members"></a>Members

 **ulFlags**
  
> 予約されています。0 にする必要があります。
    
 **ulMVPropTag**
  
> PT_MV_TSTRING の種類の複数値を持つプロパティのプロパティ タグです。 このプロパティの値は、ドロップ ダウン リストの個別のエントリとして表示されます。
    
## <a name="remarks"></a>注釈

**DTBLMVDDLBOX**構造体では、複数値を持つドロップ ダウン リスト項目の読み取り専用の一覧について説明します。 複数値を持つドロップ ダウン リストを使用すると、ユーザーがスクロール バーをクリックすると値が表示されます。 
  
データが表示される**ulMVPropTag**のメンバーで識別されるプロパティに由来します。 ディスプレイ テーブルに関連付けられているプロパティのインターフェイスから参照する必要はありません。 また、ユーザーがこれらの種類のリスト ボックスから項目を選択をすることができないため、データはプロパティのインターフェイスに書き込まれません。 
  
複数値を持つドロップ ダウン リストの複数値を持つ文字列のプロパティだけがサポートされています。他の複数値を持つプロパティの型はサポートされていません。 
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

