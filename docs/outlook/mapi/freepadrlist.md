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
ms.openlocfilehash: 39a184f00ccf54d4fa4477bbdf3086f3e44bddb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576548"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
[ADRLIST](adrlist.md)構造体を破棄し、すべてのアレイ メンバーと構造体に割り当てられたメモリを含む、関連付けられているメモリを解放します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>パラメーター

 _padrlist_
  
> [in]破棄する**ADRLIST**構造体へのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**FreePadrlist**の実装の一部としては、MAPI は、完全な構造を解放する前に**ADRLIST**構造体のすべてのエントリを解放する[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。 このためこのようなすべてのエントリは[ADRLIST](adrlist.md)構造体の割り当て規則に従っている必要があります、個人を使用して[MAPIAllocateBuffer](mapiallocatebuffer.md)を各メンバーの配列と構造体を呼び出します。 
  
**ADRLIST**と**SRowSet**構造体のメモリの割り当ての詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI では、 **FreePadrlist**メソッドを使用して、1 回限りのアドレスをメッセージに追加するのには構築された ADRLIST 構造体を解放します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

