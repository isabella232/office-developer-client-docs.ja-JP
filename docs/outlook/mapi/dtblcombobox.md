---
title: DTBLCOMBOBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCOMBOBOX
api_type:
- COM
ms.assetid: 73b68614-6aca-4669-b879-5631c5d6483c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5256efbff734d4555ac263dd330e3349c789cd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406977"
---
# <a name="dtblcombobox"></a>DTBLCOMBOBOX

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから作成されたダイアログ ボックスで使用されるコンボ ボックス コントロールについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |
   
```cpp
typedef struct _DTBLCOMBOBOX
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPRPropertyName;
  ULONG ulPRTableName;
} DTBLCOMBOBOX, FAR *LPDTBLCOMBOBOX;

```

## <a name="members"></a>Members

 **ulbLpszCharsAllowed**
  
> **DTBLCOMBOBOX** 構造体の開始から、制限がある場合は、コンボ ボックスの編集コントロールに入力できる文字を表す文字列フィルターへのオフセット。 フィルターは正規表現として解釈されるのではなく、入力された文字ごとに同じフィルターが適用されます。 フィルターの形式は次のとおりです。 
    
|**文字**|**説明**|
|:-----|:-----|
| `*` <br/> |任意の文字を使用できます (たとえば  `"*"` )。  <br/> |
| `[ ]` <br/> |文字のセットを定義します (たとえば  `"[0123456789]"` )。  <br/> |
| `-` <br/> |文字の範囲を示します (たとえば  `"[a-z]"` )。  <br/> |
| `~` <br/> |これらの文字は使用できません。 (たとえば  `"[~0-9]"` )。  <br/> |
| `\` <br/> |前の記号を引用符で囲む場合に使用します (たとえば  `"[\-\\\[\]]"` \, 、-、[、] 文字を使用できます)。  <br/> |
   
 **ulFlags**
  
> 文字列フィルターの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> フィルターは Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、フィルターは ANSI 形式になります。
    
 **ulNumCharsAllowed**
  
> コンボ ボックスのテキスト ボックスに入力できる最大文字数。
    
 **ulPRPropertyName**
  
> 型のプロパティのプロパティ タグPT_TSTRING。 
    
 **ulPRTableName**
  
> **OpenProperty** 呼び出しをPT_OBJECT **IMAPITable** インターフェイスを開くことができる型のプロパティのプロパティ タグ。 表には **、ulPRPropertyName** メンバーで識別されるプロパティと同じ型のプロパティを持つ列が 1 つ必要です。 テーブルの行を使用して、リストに値を設定します。 
    
## <a name="remarks"></a>注釈

**DTBLCOMBOBOX** 構造体は、リストと選択フィールドで構成されるコントロールをコンボ ボックスで表します。 リストには、ユーザーが選択できる情報が表示され、選択フィールドに現在の選択範囲が表示されます。 選択フィールドは編集コントロールで、リストにテキストを入力していない場合にも使用できます。 
  
2 つのプロパティ タグ メンバーが連携して、リスト表示を編集コントロールと調整します。 MAPI が最初にコンボ ボックスを表示すると、表示テーブルに関連付けられた **IMAPIProp** 実装の **OpenProperty** メソッドを呼び出して **、ulPRTableName** メンバーで表されるテーブルを取得します。 このテーブルには **、ulPRPropertyName** メンバーで表されるプロパティの値を含む列が 1 つ含まれます。 したがって、この列は **ulPRPropertyName** プロパティと同じ型である必要があります。両方の列は文字列である必要があります。 
  
列の値は、コンボ ボックスのリスト セクションに表示されます。 したがって **、PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) は **ulPRPropertyName** の有効なプロパティ タグではありません。 ユーザーがいずれかの行を選択するか、テキスト ボックスに新しいデータを入力すると **、ulPRPropertyName** プロパティは選択または入力された値に設定されます。 
  
編集コントロールの初期値を表示するには、MAPI は [IMAPIProp::GetProps](imapiprop-getprops.md) を呼び出して、表示テーブルのプロパティ値を取得します。 取得されたプロパティの 1 つが **ulPRPropertyName** メンバーで表されるプロパティと一致する場合、その値は初期値になります。 
  
表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。 表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)
  
[PidTagControlType 標準プロパティ](pidtagcontroltype-canonical-property.md)


[MAPI の構造](mapi-structures.md)

