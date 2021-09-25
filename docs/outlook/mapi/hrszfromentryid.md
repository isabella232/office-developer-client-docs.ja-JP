---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3f6731653fdfde158a0a03b8fa3824b39f882dc1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584508"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
エントリ識別子を ASCII 文字列にエンコードします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>パラメーター

 _cb_
  
> [in]  _pentry_ パラメーターが指すエントリ識別子のサイズ (バイト単位)。 
    
 _pentry_
  
> [in]エンコードするエントリ識別子を含む [ENTRYID](entryid.md) 構造体へのポインター。 
    
 _psz_
  
> [out]返される ASCII 文字列へのポインター。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

[HrEntryIDFromSz](hrentryidfromsz.md)関数と **HrSzFromEntryID** 関数は、エントリ識別子の文字列形式とバイナリ形式の間の変換を提供します。 MAPI では、バイナリ データで構造体を使用する必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**HrSzFromEntryID** 関数は [、MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して ASCII 文字列のメモリを割り当てる。 
  

