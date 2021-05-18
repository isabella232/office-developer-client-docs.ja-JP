---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407257"
---
# <a name="srowset"></a>SRowSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
SRow 構造体の [配列を格納](srow.md) します。 各 **SRow** 構造体は、テーブルの行を表します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbNewSRowSet](cbnewsrowset.md)、 [CbSRowSet](cbsrowset.md)、 [SizedSRowSet](sizedsrowset.md) <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a>Members

 **cRows**
  
> aRow **メンバー内** の **SRow 構造体の** 数。 
    
 **aRow**
  
> **SRow 構造体の** 配列。 テーブル内の行ごとに 1 つの構造があります。 
    
## <a name="remarks"></a>注釈

**SRowSet 構造体は**、テーブルから複数行のデータを記述するために使用されます。 **SRowSet** 構造体は、次の機能に加えて [、IAddrBook、ITableData、](iaddrbookimapiprop.md)[および IMAPITable](imapitableiunknown.md)インターフェイス メソッドで使用されます。 [](itabledataiunknown.md) 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 **SRowSet** 構造体は、受信者テーブルの行とアドレス一覧内のエントリを同じ扱いを可能にするために [、ADRLIST](adrlist.md) 構造と同じように定義されます。 **SRowSet 構造体と** **ADRLIST** 構造体の両方を [、IMessage::ModifyRecipients](imessage-modifyrecipients.md)や [IAddrBook::Address などのメソッドに渡す場合があります](iaddrbook-address.md)。 
  
また **、SRowSet** 構造体のメモリ割り当てのルールは **、ADRLIST 構造体の場合と同** じです。 要約すると、行セット内の各行の **lpProps** メンバーが指す配列内の [各 SPropValue](spropvalue.md)構造体は [、MAPIAllocateBuffer](mapiallocatebuffer.md)を使用して個別に割り当てる必要があります。 各プロパティ値の構造体は、割り当てられた **SPropValue** 構造体へのポインターが失われずに **、SRowSet** 構造体の割り当て解除の前に [MAPIFreeBuffer](mapifreebuffer.md)を使用して割り当て解除する必要があります。 その後、行の割り当てられたメモリを保持し **、SRowSet** 構造体のコンテキスト外で再利用できます。 
  
**SRowSet** 構造体のメモリを割り当てる方法の詳細については [、「ADRLIST および SRowSet 構造体](managing-memory-for-adrlist-and-srowset-structures.md)のメモリの管理」を参照してください。 
  
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[MAPI の構造](mapi-structures.md)

