---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 331dc05b30390bb803d186f157e0fe9edb779ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571669"
---
# <a name="ssortorder"></a>SSortOrder
 
**適用されます**: Outlook 2013 |Outlook 2016 
  
並べ替えキー、および並べ替えの方向として使用するには、どのような列、テーブルの行をソートする方法を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a>Members

**ulPropTag**
  
> キー、または、カテゴリ別の並べ替え、[カテゴリ] 列の並べ替えを識別するプロパティ タグです。
    
**ulOrder**
  
> データの並べ替え順序です。 使用可能な値は次のとおりです。
    
  - TABLE_SORT_ASCEND: テーブルを昇順で並べ替えする必要があります。
      
  - TABLE_SORT_COMBINE: 並べ替え操作は、以前の**SSortOrder**構造体で指定した並べ替えキー列を持つ**ulPropTag**のメンバーの並べ替えキー列として識別されるプロパティを結合するカテゴリを作成する必要があります。 
      
    TABLE_SORT_COMBINE は、 **SSortOrder**構造体は、カテゴリ別の並べ替えのさまざまな並べ替え順序を指定する[SSortOrderSet](ssortorderset.md)構造体のエントリとして使用されている場合にのみ使用できます。 TABLE_SORT_COMBINE は、 **SSortOrderSet**構造体の最初の**SSortOrder**構造体では使用できません。 
      
  - TABLE_SORT_DESCEND: テーブルの並べ替えを降順に並べ替え。
      
  - TABLE_SORT_CATEG_MAX: **SSortOrderSet**構造体の前の並べ替え順序で指定されたカテゴリ内のデータ行の**ulPropTag**メンバーの最大値でテーブルを並べ替える必要があります。 
      
  - TABLE_SORT_CATEG_MIN: 前の**SSortOrderSet**構造体の並べ替え順序で指定されたカテゴリ内のデータ行の**ulPropTag**メンバーの最小値のテーブルを並べ替える必要があります。 
    
## <a name="remarks"></a>注釈

**SSortOrder**構造体を使用して、標準的な並べ替え操作またはカテゴリ別に並べ替え操作を実行する方法について説明します。 **SSortOrder**構造体を複数の並べ替えキーと方向を記述する**SSortOrderSet**構造に組み合わせます。 **SSortOrderSet**構造体は、次の関数やインターフェイス メソッドで使用されます。 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
許可されているテーブルの列の並べ替えキーとして使用できる範囲は、プロバイダーによって異なります。 現在の列セットの一部である列は、並べ替えキーとして常に使用できます。 ただし、各プロバイダーは、現在の列ではなく設定される利用可能な列を使用して、並べ替えキーを定義できるかどうかを決定します。 列は、TBL_ALL_COLUMNS フラグが設定されている場合に、 [IMAPITable::QueryColumns](imapitable-querycolumns.md)から返される列です。 
  
**UlOrder**メンバーを示します両方の方向の順序と分類については、たとえば、テーマ ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) は、メッセージと返信の一連の会話スレッドは、別。 行は、最後に配置されたすべての NULL エントリを降順または昇順で並べ替えることができます。 
  
TABLE_SORT_COMBINE 値は、「複合」カテゴリを作成する前のカテゴリ列に**ulPropTag**で指定された列を組み合わせる必要がありますことを示します。 個々 の列の一意の値に分類することではなく TABLE_SORT_COMBINE では、列の組み合わせの一意の値に分類されます。 たとえば、特定の件名に特定の送信者から受信したメッセージをグループ化する 1 つのカテゴリを定義できます。 TABLE_SORT_COMBINE に値を設定すると、表示されているカテゴリの行の数が減少します。 
  
複数値を持つ列で並べ替えをサポートされていませんユニバーサル テーブルのすべての実装によって。 サポートされている場合は、 **ulPropTag**のメンバーで複数値を持つ列と並べ替えのキーを識別するプロパティ タグに MVI_PROP マクロを使用して MV_FLAG を適用します。 複数値を持つ列で並べ替えをすると、個々 の値を使用するのに基づいています。 
  
> [!IMPORTANT]
> **UlOrder**メンバーの値がダウンロード可能なヘッダー ファイルで TABLE_SORT_CATEG_MAX と TABLE_SORT_CATEG_MIN を定義する可能性がありますいない現在がある場合、次の値を使用してコードを追加する場合: >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
詳細については、標準的なカテゴリ別に並べ替え、[並べ替えや分類](sorting-and-categorization.md)を参照してください。 
  
## <a name="see-also"></a>関連項目

- [SSortOrderSet](ssortorderset.md)
- [MAPI の構造](mapi-structures.md)

