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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3a5188ea9f83d05722c6b5ab81d9e796b33ef254
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799969"
---
# <a name="dtblcombobox"></a>DTBLCOMBOBOX

  
  
**適用されます**: Outlook 
  
ダイアログ ボックスが表示テーブルの構築に使用するコンボ ボックス コントロールについて説明します。
  
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

## <a name="members"></a>メンバー

 **ulbLpszCharsAllowed**
  
> 場合、エディット コントロールのいずれかのコンボ ボックスに入力できる文字の制限を記述する文字の文字列のフィルターに**DTBLCOMBOBOX**構造体の先頭からオフセットします。 フィルターは正規表現として解釈されないと、入力されたすべての文字に同じフィルターを適用します。 フィルターの形式は次のとおりです。 
    
|**文字**|**説明**|
|:-----|:-----|
| `*` <br/> |任意の文字が許可される (たとえば、 `"*"`)。  <br/> |
| `[ ]` <br/> |文字のセットを定義 (たとえば、 `"[0123456789]"`)。  <br/> |
| `-` <br/> |文字の範囲を示します (たとえば、 `"[a-z]"`)。  <br/> |
| `~` <br/> |これらの文字が許可されていないことを示します。 (たとえば、 `"[~0-9]"`)。  <br/> |
| `\` <br/> |従来の記号のいずれかを引用するために使用 (たとえば、`"[\-\\\[\]]"`意味の\,[と] 文字は使用)。  <br/> |
   
 **ulFlags**
  
> 文字の文字列のフィルターの形式を指定するために使用するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> フィルターは、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のフィルターです。
    
 **ulNumCharsAllowed**
  
> コンボ ボックスのテキスト ボックスに入力できる文字の最大数。
    
 **ulPRPropertyName**
  
> 型 PT_TSTRING のプロパティのプロパティ タグです。 
    
 **ulPRTableName**
  
> **IMAPITable**インターフェイスを**OpenProperty**呼び出しを使用して開くことができる型 PT_OBJECT のプロパティのプロパティ タグです。 テーブルには、1 つの列プロパティは、 **ulPRPropertyName**のメンバーによって識別されるプロパティと同じ型を持つ必要があります。 リストを作成するテーブルの行を使用します。 
    
## <a name="remarks"></a>備考

**DTBLCOMBOBOX**構造体では、コンボ ボックスの一覧と、[選択] フィールドで構成されるコントロールについて説明します。 一覧には、情報をユーザーが選択できる、選択フィールドには、現在の選択範囲が表示されますが表示されます。 選択フィールドは、エディット コントロールにテキストを入力されていないリストも使用できます。 
  
エディット コントロールにリストの表示を調整するため 2 つのプロパティ タグのメンバーが連携して動作します。 MAPI には、まず、コンボ ボックスが表示されたら、 **ulPRTableName**のメンバーによって表されるテーブルを取得するために表示された表に関連付けられている**IMAPIProp**実装の**OpenProperty**メソッドを呼び出します。 このテーブルは、 **ulPRPropertyName**のメンバーによって表されるプロパティの値を含む列を 1 つの列にあります。 したがって、 **ulPRPropertyName**プロパティと同じ型のこの列がある必要があり、両方の列は文字列である必要があります。 
  
列の値は、コンボ ボックスのリスト] セクションに表示されます。 したがって、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) は、 **ulPRPropertyName**のプロパティの有効なタグではありません。 ユーザーは、行のいずれかを選択するか、テキスト ボックスに新しいデータを入力、すると、 **ulPRPropertyName**プロパティは、選択または入力した値に設定されます。 
  
エディット コントロールの初期値を表示するには、MAPI は、表示された表のプロパティ値を取得するために[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出します。 取得したプロパティのいずれかには、 **ulPRPropertyName**のメンバーによって表されるプロパティが一致すると、その値が初期値になります。 
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)
  
[PidTagControlType の標準的なプロパティ](pidtagcontroltype-canonical-property.md)


[MAPI の構造](mapi-structures.md)

