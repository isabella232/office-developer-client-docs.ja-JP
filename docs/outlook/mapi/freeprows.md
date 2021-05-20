---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b1109b3201e1b1e4a78c3a0fe0f2eb4d0cd43c05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438821"
---
# <a name="freeprows"></a>FreeProws

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[SRowSet 構造体を破棄し](srowset.md)、すべてのメンバー配列と構造体に割り当てられたメモリを含む、関連付けられたメモリを解放します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>パラメーター

 _prows_
  
> [in]破棄する **SRowSet** 構造体へのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**FreeProws** の実装の一環として、MAPI は [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、完全な構造を解放する前に **SRowSet** 構造体内のすべてのエントリを解放します。 したがって、このようなエントリはすべて、メンバー配列と構造体ごとに個別の[MAPIAllocateBuffer](mapiallocatebuffer.md)呼び出しを使用して[、SRowSet](srowset.md)構造体の割り当てルールに従っている必要があります。 
  
ADRLIST 構造体および **SRowSet** 構造体のメモリ割り当ての詳細については **、「ADRLIST** および SRowSet 構造体のメモリの管理」[を参照してください](managing-memory-for-adrlist-and-srowset-structures.md)。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI は **FreeProws** メソッドを使用して、処理するテーブルの行を含む SRowSet 構造体を解放します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

