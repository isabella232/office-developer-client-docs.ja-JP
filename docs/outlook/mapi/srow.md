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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2e75bc6f8e14258787a6c9d80dfbf6334ec698b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336518"
---
# <a name="srow"></a>SRow

**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のオブジェクトに対して選択されたプロパティを含むテーブルの行を記述します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
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
  
> **lpprops**メンバーが指すプロパティ値を適切に配置するためのパディングバイト。 
    
**cvalues**
  
> **lpprops**が指すプロパティ値の数。 
    
**lpprops**
  
> 行の列のプロパティ値を記述する[spropvalue](spropvalue.md)構造体の配列へのポインター。 
    
## <a name="remarks"></a>解説

**srow**構造は、テーブル内の行について記述します。 これは、テーブル通知に付随する[TABLE_NOTIFICATION](table_notification.md)構造に含まれています。 
  
**srow**構造体は、次のメソッドで使用されます。 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [itabledata: IUnknown](itabledataiunknown.md)(多くのメソッド) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
複数の行を記述する必要がある場合は、 [srowset](srowset.md)構造体を使用します。 **srowset**構造体には、 **srowset**構造の配列と、配列内の構造体の数が含まれています。 
  
次の図は、 **srow**と**srow**データ構造の関係を示しています。 
  
**SRow と SRowSet の関係**
  
![srow と srow の関係](media/amapi_17.gif "srow と srow の関係")
  
**srow**構造体は、 [adrentry](adrentry.md)構造と同じように定義されています。 したがって、受信者テーブルの行とアドレス一覧のエントリは同じ処理を行うことができます。 
  
**srow**構造のメモリを割り当てる方法については、「 [adrlist および srow 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI の構造](mapi-structures.md)
- [adrlist および srowset 構造のためのメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)

