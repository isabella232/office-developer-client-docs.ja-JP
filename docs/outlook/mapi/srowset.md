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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5c634fe200dde4bfe6f190f8bfa9e5dfa0868db4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804017"
---
# <a name="srowset"></a>SRowSet

  
  
**適用されます**: Outlook 
  
[SRow](srow.md)構造体の配列が含まれています。 各**SRow**構造体では、テーブルからの行について説明します。 
  
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

## <a name="members"></a>メンバー

 **カラス**
  
> **ARow**メンバーに**SRow**構造体の数です。 
    
 **aRow**
  
> **SRow**構造体の配列です。 テーブル内の行ごとに 1 つの構造があります。 
    
## <a name="remarks"></a>備考

**SRowSet**構造体を使用して、複数のテーブルからデータ行を記述します。 **SRowSet**構造体は、次の関数だけでなく、 [IAddrBook](iaddrbookimapiprop.md)、 [ITableData](itabledataiunknown.md)、および[IMAPITable](imapitableiunknown.md)インターフェイス メソッドで使用されます。 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 **SRowSet**構造体を定義するアドレス一覧に受信者テーブルおよびエントリの行を許可する[ADRLIST](adrlist.md)構造体を同等に扱うのと同じです。 **SRowSet**構造体と構造体の**ADRLIST**の両方は、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)や[IAddrBook::Address](iaddrbook-address.md)などのメソッドに渡すことができます。 
  
また、 **SRowSet**構造体のメモリの割り当て規則は、 **ADRLIST**構造体の場合と同じです。 要約するは[MAPIAllocateBuffer](mapiallocatebuffer.md)を使用して個別に、行の行ごとの**lpProps**のメンバーによって設定するのには配列内の各[SPropValue](spropvalue.md)構造体を割り当てる必要があります。 **SRowSet**構造の割り当てを解除する前に割り当てられた**SPropValue**構造体へのポインターが失われないように[MAPIFreeBuffer](mapifreebuffer.md)を使用して各プロパティ値の構造体を解放することもする必要があります。 行のメモリが割り当てられているし、ある保持し、 **SRowSet**構造体のコンテキストの外部で再利用します。 
  
**SRowSet**構造体のメモリの割り当て方法の詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[MAPI の構造](mapi-structures.md)

