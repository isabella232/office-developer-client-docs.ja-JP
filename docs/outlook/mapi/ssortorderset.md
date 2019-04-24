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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: db19c3908c419b98b8deb71e2a86d0aa6eebe240
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344423"
---
# <a name="ssortorderset"></a>SSortOrderSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
標準または分類された並べ替えに使用されるテーブルの並べ替えキーのコレクションを定義します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbNewSSortOrderSet](cbnewssortorderset.md)、 [cbssortorderset](cbssortorderset.md)、 [sizedssortorderset](sizedssortorderset.md) <br/> |
   
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

 **csorts**
  
> **asort**メンバに含まれている、 [ssortorder](ssortorder.md)構造の数。 
    
 **ccategories**
  
> カテゴリ列として指定されている列の数。 指定できる値は、分類されていない、または標準の並べ替えを示す0から、 **csorts**メンバーによって示される番号までです。 
    
 **cexpanded**
  
> 展開状態で開始されるカテゴリの数。これにより、カテゴリに適用されるすべての行がテーブルビューに表示されます。 指定可能な値の範囲は、0から**ccategories**で示されている数までです。
    
 **asort**
  
> ソート順序を定義する、 **ssortorder**構造の配列。 
    
## <a name="remarks"></a>解説

**ssortorderset**構造は、標準および分類された並べ替えに対して複数の並べ替え順序を定義するために使用されます。 
  
各**ssortorderset**構造には、並べ替え**** の方向と、並べ替えキーとして使用される列を定義する、少なくとも1つの sorderstructure が含まれています。 分類された並べ替えの場合、この列はカテゴリとして使用されます。 csorts メンバーの値**** が**csorts**メンバーの値を超えると、カテゴリよりも多くの並べ替えキーが存在し、その列から、 **ssortorder**配列の先頭に表示されている列に分類項目が作成されます。 
  
たとえば、csorts **** が3に設定されていて、 **csorts**が2に設定されている場合、 **ssortorder**配列の最初の2つのエントリの**ulPropTag**メンバによって記述されている列は、カテゴリ列として使用されます。 最初のエントリは、トップレベルのカテゴリグループとして機能します。2番目のエントリを第2のグループにします。 2つのカテゴリ列に一致するすべての行は、3番目のエントリで定義されている並べ替えキーを使用して並べ替えられます。 
  
**cexpanded**メンバーは、最初に展開されたカテゴリの数を指定します。 カテゴリが複数ある場合、テーブルの実装は、カテゴリとして指定された最初の列から始まり、 **ccategories**の数を超えない限り、後続のカテゴリの列と連続した順序で続きます。 拡張された列の数よりも多くのカテゴリ列がある場合は、カテゴリ列は折りたたまれています。 **cexpanded**が0の場合は、表のユーザーが表示に使用できるのは最上位レベルの見出し行だけです。 **cexpanded**がカテゴリの数よりも小さい値に等しい場合は、すべての見出し行とリーフ行のいずれも使用できません。 **cexpanded**がカテゴリの数と等しい場合、テーブルは完全に展開されます。 
  
標準および分類された並べ替えの詳細については、「[並べ替えと分類](sorting-and-categorization.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[MAPI の構造](mapi-structures.md)

