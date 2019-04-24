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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f3d98a3133d79f78f4eb676d49ec85ef5a359f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340118"
---
# <a name="dtblpage"></a>DTBLPAGE

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから構築されたダイアログボックスで使用されるタブページについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
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

 **ulblpszlabel**
  
> [ページ] タブの文字文字列ラベルのメモリ内での位置を指定します。
    
 **ulFlags**
  
> **ulblpszlabelname**メンバーによって示されるラベルの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。 
    
MAPI_UNICODE 
  
> ラベルは Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、ラベルは ANSI 形式になります。
    
 **ulblpszcomponent**
  
> mapisvc.inf の **[Help File Mappings]** セクションを識別する文字列のメモリ内での位置を指定します。INF 構成ファイルまたは0。 mapisvc.inf に表示されるファイル名。INF セクションは、ユーザーがダイアログボックスの [**ヘルプ**] ボタンをクリックして、タブページの拡張ヘルプにアクセスするために使用できます。 mapisvc.inf のエントリの詳細については、を参照してください。INF については、「 [File Format of mapisvc.inf」を参照してください。INF](file-format-of-mapisvc-inf.md)。
    
 **ulcontext**
  
> **ulblpszcomponent**メンバーによって定義された文字列内のタブページの一意識別子。 [**ヘルプ**] ボタンが機能するためには、 **ulblpszcomponent**メンバーと**ulcontext**メンバーの両方が0以外である必要があります。 この識別子が0で、コンポーネントの文字列が NULL の場合、ページに関連付けられたヘルプはありません。 
    
## <a name="remarks"></a>解説

**dtblpage**構造体は、複数の関連するダイアログボックスを区切るために使用されるコントロールをタブページとして記述します。 通常、これらのダイアログボックスは、構成、メッセージ、または受信者のオプションを表示するためのプロパティシートです。 タブをクリックすると、ユーザーは1つのシートから別のシートに切り替えることができます。 
  
コンポーネントの文字列とコンテキストの識別子は、タブ付きページで拡張ヘルプを使用できるかどうかに関する情報を提供します。 拡張ヘルプが利用可能な場合は、コンポーネントの文字列とコンテキストの識別子によって、そのアクセス方法に関する情報が得られます。 コンポーネントの文字列は、ヘルプファイルにマップされます。コンテキスト識別子は、最初のヘルプトピックにマップされます。 コンテキスト識別子が0で、コンポーネント文字列が NULL の場合、拡張ヘルプは使用できません。
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

