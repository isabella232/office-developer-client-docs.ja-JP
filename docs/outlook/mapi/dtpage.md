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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ad8aec8d015849965bea6ac011c8a45e75c69ca1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408223"
---
# <a name="dtpage"></a>DTPAGE

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[builddisplaytable](builddisplaytable.md)関数によって表示テーブルから構築されたダイアログボックスについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
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
  
> **lpctl**メンバーが指すコントロールの数。 
    
 **lpszresourcename**
  
> ダイアログボックスリソースの名前または整数識別子へのポインター。 
    
 **lpszcomponent**
  
> mapisvc.inf の **[Help File Mappings]** セクションに表示される文字列へのポインター。 **lpszcomponent**は**ulitemid**メンバーとの和集合に含まれているため、これらのメンバーのうち1つだけが有効なデータを持っています。 
    
 **ulitemid**
  
> ヘルプファイル名を読み取ることができる65535以下の値を持つ整数リソース識別子。 **ulitemid**は**lpszcomponent**メンバーと共用されているため、これらのメンバーのうち1つだけが有効なデータを持っています。 
    
 **lpctl**
  
> [DTCTL](dtctl.md)構造体の配列へのポインター。ページ上の各コントロールに対して1つ。 
    
## <a name="remarks"></a>注釈

タブページのヘルプファイルを識別するには、 **lpszcomponent**メンバーをハードコーディングされた文字列または**ulitemid**メンバーのいずれかを整数リソース識別子に設定します。 
  
mapisvc.inf の **[Help File Mappings]** セクションの各エントリ。INF は、30文字以内のコンポーネント文字列から構成され、左側には右に、ヘルプファイルのパスが表示されます。 **ulitemid**と**lpszresourcename**の両方が**builddisplaytable**の_hInstance_パラメーターにあります。 詳細については、「mapisvc.inf」を参照してください[。INF [Help File Mappings] セクション](mapisvc-inf-help-file-mappings-section.md)
  
**builddisplaytable**は、この構造を使用して、コントロールリソースから表示テーブルを作成しますが、 **dtpage**構造は表示テーブル自体には表示されません。 
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

