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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b07ea265b5dcc6b9a9abb15c6be7ac9e0f94e8ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404681"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから作成されたダイアログ ボックスで使用される編集コントロールについて説明します。
  
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

## <a name="members"></a>Members

 **ulbLpszCharsAllowed**
  
> **DTBLEDIT** 構造体の開始から、制限がある場合は、編集コントロールに入力できる文字を表す文字列フィルターへのオフセット。 フィルターは正規表現として解釈されるのではなく、入力された文字ごとに同じフィルターが適用されます。 フィルターの形式は次のとおりです。 
    
|**文字**|**説明**|
|:-----|:-----|
| `*` <br/> |任意の文字を使用できます (たとえば  `"*"` )。  <br/> |
| `[ ]` <br/> |文字のセットを定義します (たとえば  `"[0123456789]".` 、 )  <br/> |
| `-` <br/> |文字の範囲を示します (たとえば  `"[a-z]"` )。  <br/> |
| `~` <br/> |これらの文字は使用できません (たとえば  `"[~0-9]"` )。  <br/> |
| `\` <br/> |前の記号を引用符で囲む場合に使用します (たとえば  `"[\-\\\[\]]"` \, 、-、[、] 文字を使用できます)。  <br/> |
   
 **ulFlags**
  
> 文字フィルターの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE
  
> フィルターは Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、フィルターは ANSI 形式になります。
    
 **ulNumCharsAllowed**
  
> ユーザーがテキスト ボックスに入力できる最大文字数。
    
 **ulPropTag**
  
> 型のプロパティのプロパティ タグPT_TSTRING。 **ulPropTag メンバーは**、編集コントロールでデータが表示および編集される文字列プロパティを識別します。 
    
## <a name="remarks"></a>注釈

**DTBLEDIT 構造体は**、英数字の情報を含むダイアログ ボックスの領域を編集コントロールに記述します。 ほとんどすべてのダイアログ ボックスには、少なくとも 1 つの編集コントロールがあります。 編集コントロールは、ユーザーが変更したり、読み取り専用にしたりできます。 
  
編集コントロールには、単一行または複数行を指定できます。 複数行の編集コントロールには、通常、スクロール バーが関連付けられている。 
  
表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。 表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[PidTagControlType 標準プロパティ](pidtagcontroltype-canonical-property.md)


[MAPI の構造](mapi-structures.md)

