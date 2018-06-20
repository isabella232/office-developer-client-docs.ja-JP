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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8b4e090b3dd6bf8ecd2517dee57093106147e22d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804004"
---
# <a name="srow"></a>SRow

**適用されます**: Outlook 
  
特定のオブジェクトの選択したプロパティを含むテーブルから行を説明します。 
  
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
  
> 埋め込みプロパティの値を正しく配置するのにはバイトで示される**lpProps**のメンバーです。 
    
**あう**
  
> **LpProps**で指定されたプロパティ値の数。 
    
**lpProps**
  
> 行の列のプロパティ値を記述する[SPropValue](spropvalue.md)構造体の配列へのポインター。 
    
## <a name="remarks"></a>備考

**SRow**構造体では、テーブル内の行について説明します。 それはテーブルの通知に付随する[TABLE_NOTIFICATION](table_notification.md)構造体に含まれます。 
  
**SRow**構造体は、次の方法で使用されます。 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [ITableData: IUnknown](itabledataiunknown.md)(多くの方法) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
複数の行を説明する必要がある、 [SRowSet](srowset.md)構造体が使用されます。 **SRowSet**構造体には、 **SRow**構造体の配列と、配列内の構造体の数が含まれています。 
  
**SRow**と**SRowSet**のデータ構造間の関係を次の図に示します。 
  
**SRow と SRowSet との関係**
  
![SRow と SRowSet との関係](media/amapi_17.gif "SRow と SRowSet との関係")
  
**SRow**構造体が定義されている[ADRENTRY](adrentry.md)構造体と同じです。 受信者テーブルと、[アドレス] ボックスの一覧内のエントリの行は、そのため、同じに扱われます。 
  
**SRow**構造体のメモリの割り当て方法については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI の構造](mapi-structures.md)
- [ADRLIST および SRowSet 構造体のメモリを管理します。](managing-memory-for-adrlist-and-srowset-structures.md)

