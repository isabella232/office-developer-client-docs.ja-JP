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
ms.openlocfilehash: bd0caff8a6c7834bdd01ef4be64805bde66dd6d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578823"
---
# <a name="dtblpage"></a>DTBLPAGE

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ディスプレイ テーブルから組み込まれているダイアログ ボックスで使用するタブ付きのページを説明します。 
  
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
  
> ページ タブの文字の文字列のラベルのメモリ内の位置。
    
 **ulFlags**
  
> **UlbLpszLabelName**メンバーで指定されたラベルの書式を指定するために使用するフラグのビットマスクです。 次のフラグを設定することができます。 
    
MAPI_UNICODE 
  
> ラベルは、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のラベルです。
    
 **ulbLpszComponent**
  
> **[ヘルプ ファイルのマッピング]** セクションで、MAPISVC を識別する文字列のメモリ内の位置。INF ファイルを構成、または 0。 MAPISVC に表示されるファイル名です。INF セクション] ダイアログ ボックスの [**ヘルプ**] ボタンをクリックすると、タブ付きページの拡張ヘルプにアクセスするユーザーが使用できます。 MAPISVC 内のエントリに関する詳細については。INF、[形式の MAPISVC にファイルを参照してください。INF](file-format-of-mapisvc-inf.md)。
    
 **ulContext**
  
> **UlbLpszComponent**のメンバーによって定義されている文字列のタブ付きページの一意の識別子です。 **UlbLpszComponent**メンバーと**ulContext**のメンバーの両方を操作するのには [**ヘルプ**] ボタンを 0 以外の値にする必要があります。 この識別子は 0 をし、コンポーネントの文字列が NULL の場合、ページに関連付けられているヘルプはありません。 
    
## <a name="remarks"></a>注釈

**DTBLPAGE**構造体では、タブ付きページの関連するダイアログ ボックスがいくつかの区切りに使用するコントロールについて説明します。 通常、これらのダイアログ ボックスは、構成、メッセージ、または受信者のオプションを表示するためのプロパティ シートです。 タブをクリックすると、ユーザーは別に 1 つのシートからに切り替えることができます。 
  
コンポーネントと文字列のコンテキストの識別子では、詳しいヘルプは、タブ付きページで使用できるかどうかに関する情報を提供します。 拡張ヘルプが利用可能な場合は、コンポーネントの文字列とコンテキストの識別子はへのアクセス方法に関する情報を提供します。 コンポーネントの文字列は、ヘルプ ファイルにマップします。初期のヘルプ トピックのコンテキストの識別子にマップします。 コンテキスト id は、0 され、コンポーネントの文字列が NULL の場合、拡張ヘルプは使用できません。
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

