---
title: DTBLPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLPAGE
api_type:
- COM
ms.assetid: f899f434-a5d7-4b4f-98f9-c14c9f21b24b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f3d98a3133d79f78f4eb676d49ec85ef5a359f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424001"
---
# <a name="dtblpage"></a>DTBLPAGE

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから作成されたダイアログ ボックスで使用されるタブ付きページについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> ページ タブの文字列ラベルのメモリ内の位置。
    
 **ulFlags**
  
> **ulbLpszLabelName** メンバーが指すラベルの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。 
    
MAPI_UNICODE 
  
> ラベルは Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、ラベルは ANSI 形式になります。
    
 **ulbLpszComponent**
  
> MAPISVC の [ヘルプ ファイル マッピング **]** セクションを識別する文字列のメモリ内の位置。INF 構成ファイルまたは 0。 MAPISVC に表示されるファイル名。INF セクションを使用すると、ダイアログ ボックスの [ヘルプ] ボタンをクリックして、タブ付きページの拡張ヘルプにアクセスできます。 MAPISVC のエントリの詳細については、次の情報を参照してください。[INF、「MAPISVC のファイル形式」を参照してください。INF .](file-format-of-mapisvc-inf.md)
    
 **ulContext**
  
> **ulbLpszComponent** メンバーによって定義された文字列内のタブ付きページの一意の識別子。 ヘルプ **ボタンが機能するには、ulbLpszComponent** メンバーと **ulContext** メンバーの両方が **0** 以外である必要があります。 この識別子が 0 で、コンポーネント文字列が NULL の場合、ページに関連付けられたヘルプはありません。 
    
## <a name="remarks"></a>注釈

**DTBLPAGE 構造は**、複数の関連するダイアログ ボックスを分離するために使用されるタブ付きページを表します。 通常、これらのダイアログ ボックスは、構成、メッセージ、または受信者のオプションを表示するためのプロパティ シートです。 タブをクリックすると、ユーザーはシート間で切り替えます。 
  
コンポーネントの文字列とコンテキスト識別子は、タブ付きページで拡張ヘルプを使用できるかどうかに関する情報を提供します。 拡張ヘルプが使用可能な場合、コンポーネント文字列とコンテキスト識別子は、そのヘルプにアクセスする方法に関する情報を提供します。 コンポーネント文字列はヘルプ ファイルにマップされます。コンテキスト識別子は、最初のヘルプ トピックにマップされます。 コンテキスト識別子が 0 で、コンポーネント文字列が NULL の場合、拡張ヘルプは使用できません。
  
表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。 表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

