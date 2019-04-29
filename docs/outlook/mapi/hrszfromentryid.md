---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411555"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
エントリ識別子を ASCII 文字列にエンコードします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
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
  
> 順番_pentry_パラメーターによって指定されたエントリ識別子のサイズ (バイト単位)。 
    
 _pentry_
  
> 順番エンコードするエントリ識別子を含む[ENTRYID](entryid.md)構造体へのポインター。 
    
 _psz_
  
> 読み上げ返された ASCII 文字列へのポインター。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

[HrEntryIDFromSz](hrentryidfromsz.md)および**hrszfromentryid**関数は、エントリ識別子の文字列形式とバイナリ形式の間の変換を提供します。 MAPI では、バイナリデータで構造体を使用する必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**hrszfromentryid**関数は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して ASCII 文字列のメモリを割り当てます。 
  

