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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a187245b2594282bc9908b3075852440f418af2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800006"
---
# <a name="dtpage"></a>DTPAGE

  
  
**適用されます**: Outlook 
  
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

## <a name="members"></a>メンバー

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
    
## <a name="remarks"></a>備考

タブ付きページのヘルプ ファイルを特定するには、整数リソース識別子にハード コーディングされた文字列への**lpszComponent**のメンバーまたは**ulItemID**のメンバーのいずれかを設定します。 
  
**[ヘルプ ファイルのマッピング]** セクションには、MAPISVC 内の各エントリで、です。INF は、コンポーネント、文字列の左側と右側のヘルプ ファイルのパスに、30 文字以内で構成されています。 _HInstance_のパラメーター **BuildDisplayTable**は、 **ulItemID**と**lpszResourceName**の両方を参照ください。 詳細については、 [MAPISVC を参照してください。INF の [ヘルプ ファイルのマッピング] セクションで](mapisvc-inf-help-file-mappings-section.md)。
  
**BuildDisplayTable**では、この構造体を使用して、テーブルを作成、表示コントロールのリソースから表示テーブル自体に**DTPAGE**構造は表示されません。 
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)
