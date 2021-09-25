---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1422a8f6568c210c2d4416a58f625cc701ca3616
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571949"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ASCII エンコードからエントリ識別子を再作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a>パラメーター

 _sz_
  
> [in]エントリ識別子を作成する ASCII 文字列へのポインター。 
    
 _pcb_
  
> [out]  _ppentry_ パラメーターが指すエントリ識別子のサイズ (バイト単位) へのポインター。 
    
 _ppentry_
  
> [out]新しいエントリ識別子を含む、返 [される ENTRYID](entryid.md) 構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> レクリエーションは成功しました。
    
MAPI_E_INVALID_ENTRYID
  
> エントリ ID が無効でした。
    
## <a name="remarks"></a>注釈

**HrEntryIDFromSz** 関数と [HrSzFromEntryID](hrszfromentryid.md)関数は、エントリ識別子の文字列形式とバイナリ形式の間の変換を提供します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**HrEntryIDFromSz** 関数は [、MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して ASCII 文字列のメモリを割り当てる。 
  

