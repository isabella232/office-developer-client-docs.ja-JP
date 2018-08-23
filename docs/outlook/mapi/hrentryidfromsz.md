---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2b7ef789c80f85f3539ec3bbd0caf4a8adc50f3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800297"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**適用対象**: Outlook 
  
ASCII エンコードからエントリ識別子を再作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a>パラメーター

 _sz_
  
> [in]エントリ識別子を作成するから ASCII 文字列へのポインター。 
    
 _pcb_
  
> [out]_Ppentry_パラメーターで指定されたエントリの識別子のバイト単位のサイズへのポインター。 
    
 _ppentry_
  
> [out]新しいエントリの識別子を格納する返される[エントリ ID](entryid.md)の構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> 再作成に成功しました。
    
MAPI_E_INVALID_ENTRYID
  
> エントリ ID が無効でした。
    
## <a name="remarks"></a>注釈

**HrEntryIDFromSz**と[HrSzFromEntryID](hrszfromentryid.md)関数は、文字列とエントリの識別子のバイナリ フォーマット間の変換を提供します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**HrEntryIDFromSz**関数は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して ASCII 文字列のメモリを割り当てます。 
  

