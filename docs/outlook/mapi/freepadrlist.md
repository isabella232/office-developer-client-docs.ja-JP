---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b90b6705909219acfe7337baedce105de301feb2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610945"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[ADRLIST 構造体を破棄し](adrlist.md)、関連付けられたメモリ (すべてのメンバー配列と構造体に割り当てられたメモリを含む) を解放します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>パラメーター

 _padrlist_
  
> [in]破棄する **ADRLIST** 構造体へのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**FreePadrlist** の実装の一環として、MAPI は [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して **、ADRLIST** 構造内のすべてのエントリを解放してから、完全な構造を解放します。 したがって、このようなエントリはすべて、メンバー配列と構造体ごとに個別の[MAPIAllocateBuffer](mapiallocatebuffer.md)呼び出しを使用して[、ADRLIST](adrlist.md)構造体の割り当てルールに従っている必要があります。 
  
ADRLIST 構造体および **SRowSet** 構造体のメモリ割り当ての詳細については **、「ADRLIST** および SRowSet 構造体のメモリの管理」[を参照してください](managing-memory-for-adrlist-and-srowset-structures.md)。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI は **FreePadrlist** メソッドを使用して、メッセージに 1 回きりアドレスを追加するために構築された ADRLIST 構造体を解放します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

