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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5256efbff734d4555ac263dd330e3349c789cd74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287469"
---
# <a name="dtblcombobox"></a>DTBLCOMBOBOX

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから構築されたダイアログボックスで使用されるコンボボックスコントロールを表します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
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

 **ulblpszcharsallowed**
  
> **dtblcombobox**構造体の先頭から、制限がある場合は、コンボボックスの編集コントロールに入力できる文字を表す文字列フィルターへのオフセットです。 フィルターは正規表現として解釈されず、入力されたすべての文字に同じフィルターが適用されます。 フィルターの形式は次のとおりです。 
    
|**文字**|**説明**|
|:-----|:-----|
| `*` <br/> |任意の文字を使用できます ( `"*"`例:)。  <br/> |
| `[ ]` <br/> |文字のセットを定義します (例`"[0123456789]"`:)。  <br/> |
| `-` <br/> |文字の範囲を示します (例: `"[a-z]"`)。  <br/> |
| `~` <br/> |これらの文字が許可されていないことを示します。 (例: `"[~0-9]"`)。  <br/> |
| `\` <br/> |以前の記号のいずれかを引用するために使用`"[\-\\\[\]]"`されます\, (例:-、[、および] 文字が許可されます)。  <br/> |
   
 **ulFlags**
  
> 文字文字列フィルタの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> フィルターは Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、フィルターは ANSI 形式です。
    
 **ulnumcharsallowed**
  
> コンボボックスのテキストボックスに入力できる最大文字数。
    
 **ulprpropertyname**
  
> PT_TSTRING 型のプロパティのプロパティタグ。 
    
 **ulprtablename**
  
> **openproperty**呼び出しを使用して**IMAPITable**インターフェイスを開くことができる、PT_OBJECT 型のプロパティのプロパティタグ。 このテーブルには、 **ulprpropertyname**メンバーによって識別されるプロパティと同じ型のプロパティを持つ1つの列が必要です。 表の行は、リストを作成するために使用されます。 
    
## <a name="remarks"></a>解説

**dtblcombobox**構造体は、リストと選択フィールドで構成されるコントロールをコンボボックスに記述します。 一覧には、ユーザーが選択できる情報が表示され、選択フィールドに現在の選択範囲が表示されます。 選択フィールドは、リストにまだ含まれていないテキストの入力にも使用できる編集コントロールです。 
  
2つのプロパティタグのメンバーは連携して、リストの表示と編集コントロールを調整します。 最初に、MAPI がコンボボックスを表示するときには、表示テーブルに関連付けられている**imapiprop**実装の**openproperty**メソッドを呼び出して、 **ulprtablename**メンバーで表されるテーブルを取得します。 このテーブルには、 **ulprpropertyname**メンバーによって表されるプロパティの値を含む1つの列があります。 したがって、この列は**ulprpropertyname**プロパティと同じ型である必要があり、両方の列は文字列である必要があります。 
  
列の値は、コンボボックスの [リスト] セクションに表示されます。 そのため、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) は**ulprpropertyname**の有効なプロパティタグではありません。 ユーザーがいずれかの行を選択するか、またはテキストボックスに新しいデータを入力すると、 **ulprpropertyname**プロパティが、選択または入力した値に設定されます。 
  
編集コントロールの初期値を表示するために、MAPI は[imapiprop:: GetProps](imapiprop-getprops.md)を呼び出して、表示テーブルのプロパティ値を取得します。 取得したプロパティのいずれかが**ulprpropertyname**メンバーによって表されるプロパティと一致する場合、その値は初期値となります。 
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)
  
[PidTagControlType 標準プロパティ](pidtagcontroltype-canonical-property.md)


[MAPI の構造](mapi-structures.md)

