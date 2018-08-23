---
title: DTBLRADIOBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dee12ba9da83d2167afe13d00270a900bf0d73d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799989"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**適用対象**: Outlook 
  
オプション ボタン グループの一部となる 1 つのラジオ ・ ボタンをについて説明します。 ラジオ ボタン グループは、表示された表から組み込まれているダイアログ ボックスで使用されます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLRADIOBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulcButtons;
  ULONG ulPropTag;
  long lReturnValue;
} DTBLRADIOBUTTON, FAR *LPDTBLRADIOBUTTON;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> ラジオ ・ ボタンの文字の文字列のラベルのメモリ内の位置。
    
 **ulFlags**
  
> **UlbLpszLabel**メンバーで指定されたラベルの書式を指定するために使用するフラグのビットマスクです。 次のフラグを設定することができます。 
    
MAPI_UNICODE 
  
> ラベルは、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のラベルです。
    
 **ulcButtons**
  
> ラジオ ボタン グループ内のボタンの数。 表示された表の一連の行では、グループ内の他のボタンの**DTBLRADIOBUTTON**構造体を含める必要があります。 **UlcButtons**メンバーのそれぞれの行、同じ値が含まれている必要があります。 
    
 **ulPropTag**
  
> 型 PT_LONG のプロパティのプロパティ タグです。 ラジオ ボタン グループの最初の選択は、このプロパティの初期値に基づきます。 グループ内の各ボタンには、 **ulPropTag**の同じプロパティを設定する必要があります。 
    
 **lReturnValue**
  
> 選択したボタンを識別する一意の番号です。
    
## <a name="remarks"></a>注釈

**DTBLRADIOBUTTON**構造体では、ラジオ ボタンのボタンのグループに関連付けられているボタン コントロールについて説明します。 グループ内のボタンを 1 つだけをチェックすることができます。設定するグループの他のボタンを 1 つのボタンを設定します。 
  
ボタンの数は、グループ内のラジオ ボタンの数です。 グループ内の他のオプション ボタンの構造体は、表示された表のそれ以降の行でなければなりません。 各構造体は、そのボタンの数の値が同じで必要があります。
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[MAPI の構造](mapi-structures.md)

