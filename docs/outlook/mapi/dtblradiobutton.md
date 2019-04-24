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
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339418"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ラジオボタングループの一部となる1つのラジオボタンを表します。 ラジオボタングループは、表示テーブルから構築されたダイアログボックスで使用されます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
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

 **ulblpszlabel**
  
> ラジオボタンの文字列ラベルの文字をメモリ内に配置します。
    
 **ulFlags**
  
> **ulblpszlabel**メンバーが指すラベルの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。 
    
MAPI_UNICODE 
  
> ラベルは Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、ラベルは ANSI 形式になります。
    
 **ulcbuttons**
  
> ラジオボタングループのボタン数。 グループ内の他のボタンの**dtblradiobutton**構造体は、表示テーブルの連続する行に含まれている必要があります。 これらの各行には、 **ulcbuttons**メンバーと同じ値が含まれている必要があります。 
    
 **ulPropTag**
  
> PT_LONG 型のプロパティのプロパティタグ。 ラジオボタングループでの最初の選択は、このプロパティの初期値に基づいています。 グループ内の各ボタンには、 **ulPropTag**を同じプロパティに設定する必要があります。 
    
 **lreturnvalue**
  
> 選択したボタンを識別する一意の番号です。
    
## <a name="remarks"></a>解説

**dtblradiobutton**構造体は、ボタンのグループに関連付けられているボタンコントロールのラジオボタンを表します。 グループ内の1つのボタンだけをチェックできます。1つのボタンを設定すると、グループ内の他のボタンが未設定になります。 
  
[ボタン数] は、グループ内のオプションボタンの数を示します。 グループ内の他のオプションボタンの構造は、表示テーブル内の後続の行にある必要があります。 これらの各構造体は、ボタンの数と同じ値を持つ必要があります。
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[MAPI の構造](mapi-structures.md)

