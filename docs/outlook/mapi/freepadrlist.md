---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 95c2e52760bd7d65351b4dd2091b68a43cd2f97c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328036"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[adrlist](adrlist.md)構造体を破棄し、すべてのメンバー配列および構造体に割り当てられたメモリを含む、関連するメモリを解放します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>パラメーター

 _padrlist_
  
> 順番破棄する**adrlist**構造体へのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[MAPIFreeBuffer](mapifreebuffer.md)関数は、 **freepadrlist**の実装の一環として、完全な構造を解放する前に**adrlist**構造体のすべてのエントリを解放するために呼び出します。 そのため、このようなエントリはすべて、各メンバーの配列および構造に対して個別の[MAPIAllocateBuffer](mapiallocatebuffer.md)呼び出しを使用して、 [adrlist](adrlist.md)構造の割り当てルールに従っている必要があります。 
  
**adrlist**および**srowset**構造体のメモリ割り当ての詳細については、「 [adrlist および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIABFunctions  <br/> |addoneoffaddress  <br/> |mfcmapi は、 **freepadrlist**メソッドを使用して、メッセージに1回限りのアドレスを追加するために構築された adrlist 構造を解放します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

