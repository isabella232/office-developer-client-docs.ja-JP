---
title: DTBLEDIT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d0418ac2ec5d01d58c63e4ad48a1066cc386e946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799980"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**適用されます**: Outlook 
  
ディスプレイ テーブルから作成されたダイアログ ボックスで使用するエディット コントロールについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[SizedDtblEdit](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a>メンバー

 **ulbLpszCharsAllowed**
  
> 該当する場合、エディット コントロールに入力できる文字の制限を記述する文字の文字列のフィルターに**DTBLEDIT**構造体の先頭からオフセットします。 フィルターは正規表現として解釈されないと、入力されたすべての文字に同じフィルターを適用します。 フィルターの形式は次のとおりです。 
    
|**文字**|**説明**|
|:-----|:-----|
| `*` <br/> |任意の文字が許可される (たとえば、 `"*"`)。  <br/> |
| `[ ]` <br/> |文字のセットを定義 (たとえば、 `"[0123456789]".`)  <br/> |
| `-` <br/> |文字の範囲を示します (たとえば、 `"[a-z]"`)。  <br/> |
| `~` <br/> |これらの文字が許可されていないことを示します (たとえば、 `"[~0-9]"`)。  <br/> |
| `\` <br/> |従来の記号のいずれかを引用するために使用 (たとえば、`"[\-\\\[\]]"`意味の\,[と] 文字は使用)。  <br/> |
   
 **ulFlags**
  
> 文字フィルターの形式を指定するために使用するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE
  
> フィルターは、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のフィルターです。
    
 **ulNumCharsAllowed**
  
> ユーザーがテキスト ボックスに入力できる文字の最大数。
    
 **ulPropTag**
  
> 型 PT_TSTRING のプロパティのプロパティ タグです。 **UlPropTag**メンバーは、文字列のプロパティがデータを表示および編集コントロールでは編集を識別します。 
    
## <a name="remarks"></a>備考

**DTBLEDIT**構造体は、エディット コントロールに英数字の情報を含むダイアログ ボックス上の領域を説明します。 ほぼすべてのダイアログ ボックスには、少なくとも 1 つのエディット コントロールがあります。 エディット コントロールは、ユーザーが変更可能または読み取り専用にできます。 
  
エディット コントロールを 1 つにすることもできます行または複数行の文字列です。 複数行エディット コントロールには、通常、それらに関連付けられているスクロール バーがあります。 
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[PidTagControlType の標準的なプロパティ](pidtagcontroltype-canonical-property.md)


[MAPI の構造](mapi-structures.md)

