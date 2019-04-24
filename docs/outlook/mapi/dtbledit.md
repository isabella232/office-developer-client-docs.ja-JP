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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b07ea265b5dcc6b9a9abb15c6be7ac9e0f94e8ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32251599"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから構築されたダイアログボックスで使用される編集コントロールを表します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
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

## <a name="members"></a>Members

 **ulblpszcharsallowed**
  
> 編集コントロールに入力できる文字に制限がある場合は、 **DTBLEDIT**構造の先頭から、制限を表す文字列フィルターまでのオフセット。 フィルターは正規表現として解釈されず、入力されたすべての文字に同じフィルターが適用されます。 フィルターの形式は次のとおりです。 
    
|**文字**|**説明**|
|:-----|:-----|
| `*` <br/> |任意の文字を使用できます ( `"*"`例:)。  <br/> |
| `[ ]` <br/> |文字のセットを定義します`"[0123456789]".`(例:)。  <br/> |
| `-` <br/> |文字の範囲を示します (例: `"[a-z]"`)。  <br/> |
| `~` <br/> |これらの文字が許可されていないこと`"[~0-9]"`を示します (例:)。  <br/> |
| `\` <br/> |以前の記号のいずれかを引用するために使用`"[\-\\\[\]]"`されます\, (例:-、[、および] 文字が許可されます)。  <br/> |
   
 **ulFlags**
  
> 文字フィルターの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE
  
> フィルターは Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、フィルターは ANSI 形式です。
    
 **ulnumcharsallowed**
  
> ユーザーがテキストボックスに入力できる最大文字数。
    
 **ulPropTag**
  
> PT_TSTRING 型のプロパティのプロパティタグ。 **ulPropTag**メンバーは、編集コントロールでデータを表示および編集するための文字列プロパティを識別します。 
    
## <a name="remarks"></a>解説

**DTBLEDIT**構造体には、英数字情報を含むダイアログボックスの領域の編集コントロールが記述されています。 ほとんどすべてのダイアログボックスには、少なくとも1つの編集コントロールがあります。 編集コントロールは、ユーザーまたは読み取り専用で変更できます。 
  
編集コントロールは、単一行または複数行にすることもできます。 通常、複数行の編集コントロールには、スクロールバーが関連付けられています。 
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[PidTagControlType 標準プロパティ](pidtagcontroltype-canonical-property.md)


[MAPI の構造](mapi-structures.md)

