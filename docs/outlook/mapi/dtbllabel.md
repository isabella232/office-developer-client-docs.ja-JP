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
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287161"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから作成されたダイアログボックスで使用されるラベルを記述します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連するマクロ  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Members

 **ulblpszlabelname**
  
> 文字列のラベルをメモリ内に配置します。
    
 **ulFlags**
  
> **ulblpszlabelname**メンバーによって示されるラベルの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。 
    
MAPI_UNICODE 
  
> ラベルは Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、ラベルは ANSI 形式になります。
    
## <a name="remarks"></a>解説

**dtbllabel**構造体は、別の種類のコントロールと共に表示されるラベルコントロールテキストを記述して、そのコントロールに意味を追加します。 たとえば、ほとんどの編集コントロールはラベルの隣に配置され、入力する情報の種類をユーザーに通知します。 グループボックスやラジオボタンなどの一部のコントロールは、独自のラベルを保持します。 
  
ラベルには、Windows accelerator を含めることができます。アンパサンド (&amp;) の後の文字として識別されます。 アクセスキーを押すと、表示テーブルでこのラベルの下にある、ラベルのない最初のボタン以外のコントロールにフォーカスが置かれます。
  
複数行のラベルはサポートされていません。 複数の行を表示するには、複数のラベルが必要です。
  
読み取り専用の編集コントロールとしてラベルを使用することはできません。 違いは、編集コントロールが選択され、ラベルをコピーできないことです。 
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

