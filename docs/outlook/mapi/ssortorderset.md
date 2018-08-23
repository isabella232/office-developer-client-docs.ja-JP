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
ms.openlocfilehash: 1604c4a1a0d1bf4008595b0d150b4f7eb3d1c2ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804002"
---
# <a name="ssortorderset"></a>SSortOrderSet

  
  
**適用対象**: Outlook 
  
標準またはカテゴリ別に並べ替えに使用されるテーブルの並べ替えキーのコレクションを定義します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbNewSSortOrderSet](cbnewssortorderset.md)、 [CbSSortOrderSet](cbssortorderset.md)、 [SizedSSortOrderSet](sizedssortorderset.md) <br/> |
   
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
  
> **ASort**メンバーに含まれる[SSortOrder](ssortorder.md)構造体の数です。 
    
 **cCategories**
  
> カテゴリの列として指定されている列の数。 使用可能な値の範囲は、分類なし] または [標準の並べ替えを示す、ゼロから**cSorts**のメンバーによって指定された番号です。 
    
 **cExpanded**
  
> すべてのカテゴリに該当する行がテーブル ビューに表示される、展開した状態で始まる分類の数です。 使用可能な値の範囲は、0 から**cCategories**で指定された番号です。
    
 **aSort**
  
> 並べ替え順序を定義する各**SSortOrder**の構造体の配列です。 
    
## <a name="remarks"></a>注釈

**SSortOrderSet**構造体は、標準的なカテゴリ別に並べ替えのさまざまな並べ替え順序を定義するために使用されます。 
  
**SSortOrderSet**の各構造体には、並べ替えと並べ替えキーとして使用される列の方向を定義するには、少なくとも 1 つの**SSortOrder**構造が含まれています。 カテゴリ別の並べ替えでは、この列がカテゴリとして使用されます。 **CSorts**メンバーの値は、 **cCategories**メンバーの値を超えているとカテゴリより多くの並べ替えキーがあるカテゴリは、 **SSortOrder**配列の最初に表示される列から作成されます。 
  
などの**cSorts**を 3 に設定し、 **cCategories**が 2 に設定されて、する場合は、 **SSortOrder**配列内の最初の 2 つのエントリの**ulPropTag**のメンバーが記載されている列がカテゴリの列として使用されます。 最初のエントリは、グループ化は最上位のカテゴリとして機能します。セカンダリ ・ グループと 2 番目のエントリです。 3 番目のエントリで定義されている並べ替えキーを使用してすべての列の 2 つのカテゴリと一致する行が並べ替えられます。 
  
**CExpanded**メンバーは、最初に展開される項目の数を指定します。 複数のカテゴリが存在する場合、テーブルの実装から始まり、カテゴリとして指定するのには、最初の列、まで、それ以降のカテゴリ列に順番に**cCategories**の数を超えています。 拡張された列の数よりも多くのカテゴリの列がある場合は、カテゴリの列が折りたたまれます。 **CExpanded**がゼロに等しい場合は、最上位レベルの見出しの行だけが表示のテーブルのユーザーが利用できます。 **CExpanded**の項目の数より 1 小さい値に等しい場合、し、すべての見出し行とリーフ行の [なし] を利用できます。 **CExpanded**は、カテゴリの数に等しく、し、テーブルは完全に展開します。 
  
詳細については、標準的なカテゴリ別に並べ替え、[並べ替えや分類](sorting-and-categorization.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[MAPI の構造](mapi-structures.md)

