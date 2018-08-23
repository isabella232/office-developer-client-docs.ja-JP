---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 28f6471f74fb0fcc4f7e2f4114f0790e1564e17e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799987"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**適用対象**: Outlook 
  
ディスプレイ テーブルから組み込まれているダイアログ ボックスで使用するラベルについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連マクロ  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Members

 **ulbLpszLabelName**
  
> 文字の文字列のラベルのメモリ内の位置。
    
 **ulFlags**
  
> **UlbLpszLabelName**メンバーで指定されたラベルの書式を指定するために使用するフラグのビットマスクです。 次のフラグを設定することができます。 
    
MAPI_UNICODE 
  
> ラベルは、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のラベルです。
    
## <a name="remarks"></a>注釈

**DTBLLABEL**構造体では、別の種類の意味をそのコントロールに追加するコントロールに表示されるラベル コントロールのテキストについて説明します。 たとえば、入力する情報の種類のユーザーに通知するラベルの横にあるほとんどのエディット コントロールが配置されます。 グループ ボックスやラジオ ボタンなど、いくつかのコントロールは、独自のラベルを保持します。 
  
ラベルは、アンパサンドの直後の文字として識別される、ウィンドウのアクセラレータを含めることができます (&amp;)。 アクセラレータ キーを押すと最初の nonlabel では、次の次のラベルが表示された表のボタン以外のコントロールにフォーカスを設定します。
  
複数行のラベルのサポートはありません。 複数の明細行を表示するには、複数のラベルが必要です。
  
読み取り専用のエディット コントロールとラベルを使用することはできません。 違いは、エディット コントロールを選択し、ラベルのことはできませんが、コピーされることです。 
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

