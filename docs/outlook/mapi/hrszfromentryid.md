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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1b957c02f331038ee9104f01806720d2f8e0b542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800314"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**適用対象**: Outlook 
  
エントリ識別子は、ASCII 文字列にエンコードします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>パラメーター

 _cb_
  
> [in]_終了して_パラメーターで指定されたエントリの識別子のバイト単位のサイズです。 
    
 _終了して_
  
> [in]エンコードするエントリの識別子を含む[エントリ ID](entryid.md)の構造体へのポインター。 
    
 _2 つ_
  
> [out]返される ASCII 文字列へのポインター。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

[HrEntryIDFromSz](hrentryidfromsz.md)と**HrSzFromEntryID**関数は、文字列とエントリの識別子のバイナリ フォーマット間の変換を提供します。 MAPI では、バイナリ データを含む構造体を使用してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**HrSzFromEntryID**関数は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して ASCII 文字列のメモリを割り当てます。 
  

