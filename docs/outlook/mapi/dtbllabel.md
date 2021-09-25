---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1f0bf5445404b80021350fa70c9b21c5bbbe73fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601101"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから作成されたダイアログ ボックスで使用されるラベルについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>メンバー

 **ulbLpszLabelName**
  
> 文字列ラベルのメモリ内の位置。
    
 **ulFlags**
  
> **ulbLpszLabelName** メンバーが指すラベルの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。 
    
MAPI_UNICODE 
  
> ラベルは Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、ラベルは ANSI 形式になります。
    
## <a name="remarks"></a>注釈

**DTBLLABEL 構造体** は、別の種類のコントロールと一緒に表示されるラベル コントロール テキストを表し、そのコントロールに意味を追加します。 たとえば、ほとんどの編集コントロールはラベルの横に配置され、入力する情報の種類をユーザーに通知します。 グループ ボックスやラジオ ボタンなどの一部のコントロールは、独自のラベルを保持します。 
  
ラベルには、アンパサンド () Windows文字として識別されるアクセラレータを含めできます &amp; 。 アクセラレータ キーを押すと、表示テーブルのこのラベルに続く最初の非ラベルの非ボタン コントロールにフォーカスが配置されます。
  
複数行ラベルはサポートされていません。 複数の行を表示するには、複数のラベルが必要です。
  
ラベルを読み取り専用の編集コントロールとして使用することはできません。 違いは、編集コントロールを選択してコピーできるのに対し、ラベルは選択できないことです。 
  
表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。 表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

