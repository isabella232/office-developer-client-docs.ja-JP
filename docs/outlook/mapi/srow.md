---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2e75bc6f8e14258787a6c9d80dfbf6334ec698b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410435"
---
# <a name="srow"></a>SRow

**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のオブジェクトの選択したプロパティを含むテーブルの行について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a>Members

**ulAdrEntryPad**
  
> lpProps メンバーが指すプロパティ値を適切に揃える埋 **め込みバイト** 。 
    
**cValues**
  
> lpProps が指すプロパティ **値の数** です。 
    
**lpProps**
  
> 行内の列のプロパティ値を記述する [SPropValue](spropvalue.md) 構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

**SRow 構造体は**、テーブル内の行を表します。 これは、テーブル通知に [TABLE_NOTIFICATION](table_notification.md) の構造に含まれています。 
  
**SRow** 構造体は、次のメソッドで使用されます。 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [ITableData : IUnknown](itabledataiunknown.md) (多くのメソッド) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
複数の行を記述する必要がある場合は [、SRowSet](srowset.md) 構造体が使用されます。 **SRowSet 構造体** には **、SRow** 構造体の配列と配列内の構造体の数が含まれています。 
  
次の図は **、SRow** と **SRowSet データ構造の関係を** 示しています。 
  
**SRow と SRowSet の関係**
  
![SRow と SRowSet の SRow と SRowSet](media/amapi_17.gif "")のリレーションシップ
  
**SRow** 構造体は [ADRENTRY 構造体と同じ定義](adrentry.md) です。 したがって、受信者テーブルの行とアドレス一覧内のエントリを同じように処理できます。 
  
**SRow** 構造体のメモリを割り当てる方法については [、「ADRLIST および SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)構造体のメモリの管理」を参照してください。
  
## <a name="see-also"></a>関連項目

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI の構造](mapi-structures.md)
- [ADRLIST および SRowSet 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)

