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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b1109b3201e1b1e4a78c3a0fe0f2eb4d0cd43c05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328015"
---
# <a name="freeprows"></a>FreeProws

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[srowset](srowset.md)構造を破棄し、すべてのメンバー配列および構造体に割り当てられたメモリを含む、関連するメモリを解放します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>パラメーター

 _prows_
  
> 順番破棄する**srowset**構造体へのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI の実装の一部と**** して、MAPI は[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、完全な構造を解放する前に、 **srowset**構造のすべてのエントリを解放します。 そのため、このようなすべてのエントリは、各メンバーの配列および構造に対して個別の[MAPIAllocateBuffer](mapiallocatebuffer.md)呼び出しを使用して、 [srowset](srowset.md)構造の割り当てルールに従っている必要があります。 
  
**adrlist**および**srowset**構造体のメモリ割り当ての詳細については、「 [adrlist および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl  <br/> |dwthreadの loadtable  <br/> |mfcmapi は、 **freeprows**メソッドを使用して、処理されているテーブルの行を含む srowset 構造を解放します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

