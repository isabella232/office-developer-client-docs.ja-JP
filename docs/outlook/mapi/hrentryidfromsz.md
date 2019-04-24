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
ms.openlocfilehash: ac59aeb3d650c0fbeb5bcdb580e0401cbab58ee6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347811"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
エントリ id を ASCII エンコードから再作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
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
  
> 順番エントリ識別子を作成する ASCII 文字列へのポインター。 
    
 _設計_
  
> 読み上げ_ppentry_パラメーターによって指定されたエントリ識別子のサイズ (バイト数) へのポインター。 
    
 _ppentry_
  
> 読み上げ新しいエントリ識別子を含む、返される[ENTRYID](entryid.md)構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> 再レクリエーションは成功しました。
    
MAPI_E_INVALID_ENTRYID
  
> エントリ ID が無効です。
    
## <a name="remarks"></a>解説

**HrEntryIDFromSz**および[hrszfromentryid](hrszfromentryid.md)関数は、エントリ識別子の文字列形式とバイナリ形式の間の変換を提供します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**HrEntryIDFromSz**関数は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して、ASCII 文字列のメモリを割り当てます。 
  

