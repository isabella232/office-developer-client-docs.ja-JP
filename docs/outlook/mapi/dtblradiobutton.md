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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434600"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ラジオ ボタン グループに含む 1 つのラジオ ボタンについて説明します。 ラジオ ボタン グループは、表示テーブルから作成されたダイアログ ボックスで使用されます。
  
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
  
> ラジオ ボタンの文字列ラベルのメモリ内の位置。
    
 **ulFlags**
  
> **ulbLpszLabel** メンバーが指すラベルの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。 
    
MAPI_UNICODE 
  
> ラベルは Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、ラベルは ANSI 形式になります。
    
 **ulcButtons**
  
> ラジオ ボタン グループ内のボタンの数。 グループ **内の他のボタンの DTBLRADIOBUTTON** 構造は、表示テーブルの連続する行に含まれている必要があります。 これらの各行には **、ulcButtons メンバーの同じ値を含む必要** があります。 
    
 **ulPropTag**
  
> 型のプロパティのプロパティ タグPT_LONG。 ラジオ ボタン グループの最初の選択は、このプロパティの初期値に基づいて行います。 グループ内の各ボタンには **、ulPropTag が** 同じプロパティに設定されている必要があります。 
    
 **lReturnValue**
  
> 選択したボタンを識別する一意の番号。
    
## <a name="remarks"></a>注釈

**DTBLRADIOBUTTON 構造体は**、ボタンのグループに関連付けられているボタン コントロールをラジオ ボタンで表します。 グループ内の 1 つのボタンのみをチェックできます。1 つのボタンを設定すると、グループ内の他のボタンが設定解除されます。 
  
ボタンの数は、グループ内のラジオ ボタンの数です。 グループ内の他のラジオ ボタンの構造は、表示テーブル内の後続の行にある必要があります。 これらの各構造は、ボタン数に対して同じ値を持つ必要があります。
  
表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。 表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。
  
## <a name="see-also"></a>関連項目



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[MAPI の構造](mapi-structures.md)

