---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: aec93300a567ddb9ba946ef6bd646fdd21001f3a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566424"
---
# <a name="ssortorder"></a>SSortOrder
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルの行の並べ替え方法、並べ替えキーとして使用する列、並べ替えの方向を定義します。 
  
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

## <a name="members"></a>メンバー

**ulPropTag**
  
> 並べ替えキーまたは分類された並べ替えのカテゴリ列を識別するプロパティ タグ。
    
**ulOrder**
  
> データを並べ替える順序。 指定できる値は次のとおりです。
    
  - TABLE_SORT_ASCEND: テーブルは昇順に並べ替える必要があります。
      
  - TABLE_SORT_COMBINE: 並べ替え操作では **、ulPropTag** メンバーの並べ替えキー列として識別されるプロパティと、前の **SSortOrder** 構造体で指定された並べ替えキー列を組み合わせたカテゴリを作成する必要があります。 
      
    TABLE_SORT_COMBINE **SSortOrder** 構造体を [SSortOrderSet](ssortorderset.md) 構造体のエントリとして使用して、分類された並べ替えに対して複数の並べ替え順序を指定する場合にのみ使用できます。 TABLE_SORT_COMBINE **SSortOrderSet** 構造体の最初の **SSortOrder 構造体では使用** できません。 
      
  - TABLE_SORT_DESCEND: テーブルは降順で並べ替える必要があります。
      
  - TABLE_SORT_CATEG_MAX: **SSortOrderSet** 構造体の前の並べ替え順序で指定されたカテゴリのデータ行の **ulPropTag** メンバーの最大値でテーブルを並べ替える必要があります。 
      
  - TABLE_SORT_CATEG_MIN:**テーブルは、SSortOrderSet** 構造体の前の並べ替え順序で指定されたカテゴリのデータ行の **ulPropTag** メンバーの最小値で並べ替える必要があります。 
    
## <a name="remarks"></a>注釈

**SSortOrder 構造体を** 使用して、標準の並べ替え操作または分類された並べ替え操作を実行する方法を説明します。 **SSortOrder** 構造体は通常、複数の並べ替えキーと方向を記述するために **SSortOrderSet** 構造体に組み合わされます。 **SSortOrderSet** 構造体は、次の関数およびインターフェイス メソッドで使用されます。 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
並べ替えキーとして使用できるテーブル内の列の範囲は、プロバイダーによって異なります。 現在の列セットの一部である列は、常に並べ替えキーとして使用できます。 ただし、各プロバイダーは、現在の列セットに含めされていない使用可能な列を使用して並べ替えキーを定義できるかどうかを決定します。 使用可能な列は [、IMAPITable::QueryColumns](imapitable-querycolumns.md) のフラグが設定されているときに返TBL_ALL_COLUMNS列です。 
  
**ulOrder** メンバーは、方向順序と分類の両方の情報 (たとえば、会話 ([PidTagConversationTopic)](pidtagconversationtopic-canonical-property.md)、つまり、一連のメッセージと返信である会話スレッドを示します。 行は、すべての NULL エントリが最後に配置された昇順または降順で並べ替えできます。 
  
このTABLE_SORT_COMBINEは **、ulPropTag** で指定された列を前のカテゴリ列と組み合わせて複合カテゴリを形成する必要があります。 つまり、個々の列の一意の値を分類する代わりにTABLE_SORT_COMBINE列の組み合わせの一意の値を分類できます。 たとえば、特定の件名の特定の送信者から受信したメッセージをグループ化するために、1 つのカテゴリを定義できます。 値を設定するとTABLE_SORT_COMBINE表示されるカテゴリ行の数が減らされます。 
  
複数値の列での並べ替えは、すべてのテーブル実装で汎用的にサポートされるとは言えな。 サポートされている場合は、MV_FLAG マクロMVI_PROPを **ulPropTag** メンバーのプロパティ タグに適用して、並べ替えキーを複数値の列として識別します。 複数値の列での並べ替えは、個々の値の使用に基づいて行います。 
  
> [!IMPORTANT]
> **ulOrder** メンバー値 TABLE_SORT_CATEG_MAX および TABLE_SORT_CATEG_MIN は、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は、次の値を使用してコードに追加>`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
標準の並べ替えと分類された並べ替えの詳細については、「並べ替え [と分類」を参照してください](sorting-and-categorization.md)。 
  
## <a name="see-also"></a>関連項目

- [SSortOrderSet](ssortorderset.md)
- [MAPI の構造](mapi-structures.md)

