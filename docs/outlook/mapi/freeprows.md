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
ms.openlocfilehash: 93659a28969efd0d04e9fc44f8926e89586f7773
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800125"
---
# <a name="freeprows"></a>FreeProws

  
  
**適用対象**: Outlook 
  
[SRowSet](srowset.md)構造体を破棄し、すべてのアレイ メンバーと構造体に割り当てられたメモリを含む、関連付けられているメモリを解放します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>パラメーター

 _prows_
  
> [in]破棄する**SRowSet**構造体へのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**FreeProws**の実装の一部としては、MAPI は、完全な構造を解放する前に**SRowSet**構造内のすべてのエントリを解放する[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。 このためこのようなすべてのエントリは[SRowSet](srowset.md)構造体の割り当て規則に従っている必要があります、個人を使用して[MAPIAllocateBuffer](mapiallocatebuffer.md)を各メンバーの配列と構造体を呼び出します。 
  
**ADRLIST**と**SRowSet**構造体のメモリの割り当ての詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI では、 **FreeProws**メソッドを使用して、処理するテーブルの行を含む、SRowSet 構造体を解放します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

