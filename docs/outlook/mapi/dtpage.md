---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 769ae984e4b6e8610ca7909ea2ac714d9d04d698
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589673"
---
# <a name="dtpage"></a>DTPAGE

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
[BuildDisplayTable](builddisplaytable.md)関数によって、表示された表から組み込まれているダイアログ ボックスについて説明します。 
  
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

## <a name="members"></a>Members

 **cctl**
  
> **Lpctl**メンバーで指定されたコントロールの数。 
    
 **lpszResourceName**
  
> ダイアログ ボックスのリソースの名前または整数の識別子へのポインター。 
    
 **lpszComponent**
  
> MAPISVC.INF の **[ヘルプ ファイルのマッピング]** セクションに表示される文字列へのポインター。 **LpszComponent**が**ulItemID**のメンバーを含む共用体であるため、これらのメンバーの 1 つだけが有効なデータです。 
    
 **ulItemID**
  
> ヘルプ ファイル名を読み取ることができますから 65535 以下の値を持つ整数リソース識別子。 **UlItemID**が**lpszComponent**のメンバーを含む共用体であるため、これらのメンバーの 1 つだけが有効なデータです。 
    
 **lpctl**
  
> ページ上の各コントロールのいずれかの[DTCTL](dtctl.md)構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

タブ付きページのヘルプ ファイルを特定するには、整数リソース識別子にハード コーディングされた文字列への**lpszComponent**のメンバーまたは**ulItemID**のメンバーのいずれかを設定します。 
  
**[ヘルプ ファイルのマッピング]** セクションには、MAPISVC 内の各エントリで、です。INF は、コンポーネント、文字列の左側と右側のヘルプ ファイルのパスに、30 文字以内で構成されています。 _HInstance_のパラメーター **BuildDisplayTable**は、 **ulItemID**と**lpszResourceName**の両方を参照ください。 詳細については、 [MAPISVC を参照してください。INF の [ヘルプ ファイルのマッピング] セクションで](mapisvc-inf-help-file-mappings-section.md)。
  
**BuildDisplayTable**では、この構造体を使用して、テーブルを作成、表示コントロールのリソースから表示テーブル自体に**DTPAGE**構造は表示されません。 
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

