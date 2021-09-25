---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c88cb2425e44844de4fc127a1b97ad5dc9ed851a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566494"
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

## <a name="members"></a>メンバー

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
  
![SRow と SRowSet の関係](media/amapi_17.gif "SRow と SRowSet の関係")
  
**SRow** 構造体は [ADRENTRY 構造体と同じ定義](adrentry.md) です。 したがって、受信者テーブルの行とアドレス一覧内のエントリを同じように処理できます。 
  
**SRow** 構造体のメモリを割り当てる方法については [、「ADRLIST および SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)構造体のメモリの管理」を参照してください。
  
## <a name="see-also"></a>関連項目

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI の構造](mapi-structures.md)
- [ADRLIST および SRowSet 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)

