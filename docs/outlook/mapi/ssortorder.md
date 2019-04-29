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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439724"
---
# <a name="ssortorder"></a>SSortOrder
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
表の行を並べ替える方法、並べ替えキーとして使用する列、および並べ替えの方向を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a>メンバー

**ulPropTag**
  
> プロパティタグ。並べ替えキー、または分類された並べ替えの場合は、[カテゴリ] 列を識別します。
    
**ulorder**
  
> データの並べ替え順序を指定します。 可能な値は次のとおりです。
    
  - TABLE_SORT_ASCEND: テーブルは昇順で並べ替えられている必要があります。
      
  - TABLE_SORT_COMBINE: 並べ替え操作では、 **ulPropTag**メンバーの並べ替えキーの列として識別されたプロパティを、前の構造で指定され**** た並べ替えキーの列と組み合わせたカテゴリを作成する必要があります。 
      
    TABLE_SORT_COMBINE は、ssortorderset 構造で、分類された並べ替えに対して[](ssortorderset.md)複数の並べ替え順序を指定するためのエントリとして使用されている場合にのみ使用できます。 **** TABLE_SORT_COMBINE は、 **ssortorderset**構造の最初の**ssortorder**構造では使用できません。 
      
  - TABLE_SORT_DESCEND: テーブルは降順で並べ替えられている必要があります。
      
  - TABLE_SORT_CATEG_MAX: **ssortorderset**構造で、以前の並べ替え順序で指定されたカテゴリのデータ行について、テーブルを**ulPropTag**メンバーの最大値で並べ替えます。 
      
  - TABLE_SORT_CATEG_MIN: テーブルは、 **ssortorderset**構造で、前の並べ替え順序で指定されているカテゴリのデータ行の**ulPropTag**メンバーの最小値で並べ替えられている必要があります。 
    
## <a name="remarks"></a>注釈

**ssortorder**構造は、標準の並べ替え操作または分類された並べ替え操作のどちらを実行するかを示すために使用されます。 **** sorderstructure は、通常、複数の並べ替えキーと方向を記述するために、 **ssortorderset**構造に組み込まれています。 **ssortorderset**構造体は、次の関数およびインターフェイスメソッドで使用されます。 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
並べ替えキーとして使用できるテーブルで許可されている列の範囲は、プロバイダーによって異なります。 現在の列セットの一部である列は、常に並べ替えキーとして使用できます。 ただし、各プロバイダーは、現在の列セットに含まれていない利用可能な列を使用して並べ替えキーを定義できるかどうかを判断します。 使用可能な列は、TBL_ALL_COLUMNS フラグが設定されている場合に[IMAPITable:: querycolumns](imapitable-querycolumns.md)から返される列です。 
  
**ulorder**メンバーは、双方向の順序と分類の情報 (たとえば、会話 ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))、つまり会話スレッド (一連のメッセージと返信)) を示します。 行は、すべての NULL エントリが最後に配置された昇順または降順のどちらかの順序で並べ替えることができます。 
  
TABLE_SORT_COMBINE の値は、 **ulPropTag**で指定された列が前のカテゴリの列と組み合わせて複合カテゴリを形成する必要があることを示します。 つまり、TABLE_SORT_COMBINE では、個々の列の一意の値を分類するのではなく、列の組み合わせの一意の値について分類することができます。 たとえば、特定の件名の特定の送信者から受信したメッセージをグループ化するために、1つのカテゴリを定義できます。 TABLE_SORT_COMBINE に値を設定すると、表示されるカテゴリ行の数が少なくなります。 
  
複数値を持つ列での並べ替えは、すべてのテーブル実装で汎用的にサポートされているわけではありません。 サポートされている場合は、MVI_PROP マクロを使用して MV_FLAG を**ulPropTag**メンバーの property タグに適用し、並べ替えキーを複数値を持つ列として識別します。 複数値列での並べ替えは、個々の値の使用に基づいています。 
  
> [!IMPORTANT]
> TABLE_SORT_CATEG_MAX **** および TABLE_SORT_CATEG_MIN は、現在のダウンロード可能なヘッダーファイルで定義されていない場合があります。その場合は、次の値を使用してコードに追加できます。 >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
標準および分類された並べ替えの詳細については、「[並べ替えと分類](sorting-and-categorization.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [SSortOrderSet](ssortorderset.md)
- [MAPI の構造](mapi-structures.md)

