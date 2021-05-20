---
title: SSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrderSet
api_type:
- COM
ms.assetid: e7f9be6a-92e7-44a8-93ee-b087713a31df
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: db19c3908c419b98b8deb71e2a86d0aa6eebe240
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438100"
---
# <a name="ssortorderset"></a>SSortOrderSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
標準または分類された並べ替えに使用されるテーブルの並べ替えキーのコレクションを定義します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbNewSsortOrderSet](cbnewssortorderset.md)、 [CbSSortOrderSet](cbssortorderset.md)、 [sizedSsortOrderSet](sizedssortorderset.md) <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a>Members

 **cSorts**
  
> **aSort** メンバーに含まれる [SSortOrder](ssortorder.md)構造体の数。 
    
 **cCategories**
  
> カテゴリ列として指定されている列の数。 指定できる値の範囲は、分類されていない並べ替えまたは標準の並べ替えを示す **0 から、cSorts** メンバーによって示される番号です。 
    
 **cExpanded**
  
> 展開された状態で開始するカテゴリの数。カテゴリに適用される行はすべてテーブル ビューに表示されます。 指定できる値の範囲は、0 ~ **cCategories で示される数値です**。
    
 **aSort**
  
> 並べ **替え順序を定義する SSortOrder** 構造体の配列。 
    
## <a name="remarks"></a>注釈

**SSortOrderSet** 構造体は、標準および分類された並べ替えに対して複数の並べ替え順序を定義するために使用されます。 
  
各 **SSortOrderSet** 構造体には、並べ替えの方向と並べ替えキーとして使用される列を定義する **SSortOrder** 構造体が少なくとも 1 つ含まれる。 分類された並べ替えでは、この列がカテゴリとして使用されます。 **cSorts** メンバーの値が **cCategories** メンバーの値を超えると、カテゴリよりも並べ替えキーが多く **、SSortOrder** 配列の最初に表示される列からカテゴリが作成されます。 
  
たとえば **、cSorts** が 3 に設定され **、cCategories** が 2 に設定されている場合 **、SSortOrder** 配列の最初の 2 つのエントリの **ulPropTag** メンバーによって記述された列がカテゴリ列として使用されます。 最初のエントリは、トップ レベルのカテゴリ グループとして使用されます。2 番目のエントリをセカンダリ グループ化として指定します。 2 つのカテゴリ列に一致する行はすべて、3 番目のエントリで定義されている並べ替えキーを使用して並べ替えされます。 
  
**cExpanded メンバー** は、最初に展開されるカテゴリの数を指定します。 複数のカテゴリがある場合、テーブルの実装は、カテゴリとして指定される最初の列から始まり **、cCategories** の数を超えるまで、後続のカテゴリ列の順に続きます。 展開された列よりも多くのカテゴリ列がある場合、カテゴリ列は折りたたまれます。 **cExpanded が** 0 に等しい場合、テーブル ユーザーが表示できるのは、トップ レベルの見出し行のみです。 **cExpanded が** カテゴリ数より 1 小さい場合、すべての見出し行とリーフ行は使用できません。 **cExpanded が** カテゴリの数と等しい場合、テーブルは完全に展開されます。 
  
標準の並べ替えと分類された並べ替えの詳細については、「並べ替え [と分類」を参照してください](sorting-and-categorization.md)。
  
## <a name="see-also"></a>関連項目



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[MAPI の構造](mapi-structures.md)

