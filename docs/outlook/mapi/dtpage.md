---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0bf031772c9dda44e0496f507975f26313aa452e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576332"
---
# <a name="dtpage"></a>DTPAGE

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[BuildDisplayTable](builddisplaytable.md)関数によって表示テーブルから作成されるダイアログ ボックスについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct DTPAGE
{
  ULONG cctl;
  LPSTR lpszResourceName;
  union
  {
    LPSTR lpszComponent;
    ULONG ulItemID;
  }
  LPDTCTL lpctl;
} DTPAGE, FAR *LPDTPAGE;

```

## <a name="members"></a>メンバー

 **cctl**
  
> lpctl メンバーが指す **コントロールの** 数。 
    
 **lpszResourceName**
  
> ダイアログ ボックス リソースの名前または整数識別子へのポインター。 
    
 **lpszComponent**
  
> MAPISVC.INF の [ヘルプ ファイル マッピング **]** セクションに表示される文字列へのポインター。 **lpszComponent** は **ulItemID** メンバーとの共用体にあるため、有効なデータを持つメンバーは 1 つのみです。 
    
 **ulItemID**
  
> ヘルプ ファイル名を読み取る 65535 以下の値を持つ整数リソース識別子。 **ulItemID は** **lpszComponent** メンバーとの共用体にあるため、有効なデータを持つメンバーは 1 つのみです。 
    
 **lpctl**
  
> ページ上のコントロールごとに [1 つ、DTCTL](dtctl.md) 構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

タブ付きページのヘルプ ファイルを識別するには **、lpszComponent** メンバーをハードコードされた文字列に設定するか **、ulItemID** メンバーを整数リソース識別子に設定します。 
  
MAPISVC の **[ヘルプ ファイル マッピング] セクション** の各エントリ。INF は、左側の 30 文字以内のコンポーネント文字列と、右側のヘルプ ファイル パスで構成されます。 **ulItemID と** **lpszResourceName** の両方が **、BuildDisplayTable**_の hInstance_ パラメーターに含されています。 詳細については [、「MAPISVC」を参照してください。INF [ヘルプ ファイル マッピング] セクション](mapisvc-inf-help-file-mappings-section.md).
  
**BuildDisplayTable は**、この構造を使用してコントロール リソースから表示テーブルを構築しますが **、DTPAGE** 構造は表示テーブル自体には表示されません。 
  
表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。 表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。
  
## <a name="see-also"></a>関連項目



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

