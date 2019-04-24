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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341637"
---
# <a name="srowset"></a>SRowSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[srow](srow.md)構造の配列を格納します。 各**srow**構造は、テーブルの行について記述します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbNewSRowSet](cbnewsrowset.md)、 [cbsrowset](cbsrowset.md)、 [sizedsrowset](sizedsrowset.md) <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a>Members

 **cRows**
  
> **arow**メンバーの**srow**構造のカウント。 
    
 **arow**
  
> **srow**構造の配列。 表の各行には1つの構造があります。 
    
## <a name="remarks"></a>解説

**srowset**構造体は、テーブルの複数のデータ行を記述するために使用されます。 **srowset**構造体は、次の関数に加えて、 [IAddrBook](iaddrbookimapiprop.md)、 [itabledata](itabledataiunknown.md)、および[IMAPITable](imapitableiunknown.md)インターフェイスメソッドで使用されます。 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 **srowset**構造体は[adrlist](adrlist.md)構造体と同じように定義されており、受信者テーブルの行とアドレス一覧のエントリを同じように扱うことができます。 [IMessage:: modifyrecipients](imessage-modifyrecipients.md)および[IAddrBook:: Address](iaddrbook-address.md)などのメソッドには、 **srowset**構造体と**adrlist**構造体の両方を渡すことができます。 
  
また、 **srowset**構造体のメモリ割り当ての規則は、 **adrlist**構造体の場合と同じです。 要約すると、 [MAPIAllocateBuffer](mapiallocatebuffer.md)を使用して、行セット内の各行の**lpprops**メンバが指す各[spropvalue](spropvalue.md)構造体を個別に割り当てる必要があります。 各プロパティ値構造体は、 **srowset**構造体を解放する前に[MAPIFreeBuffer](mapifreebuffer.md)を使用して割り当てを解除して、割り当てられた**spropvalue**構造体へのポインターが失われないようにする必要があります。 行の割り当てられたメモリは保持され、 **srowset**構造のコンテキスト外で再利用できます。 
  
**srowset**構造体のメモリを割り当てる方法の詳細については、「 [adrlist および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[MAPI の構造](mapi-structures.md)

