---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a00a9b2200f76dfd600f72bf387467b5792599c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803807"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**適用されます**: Outlook 
  
16 進数の文字列形式の指定部分を 2 進数に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Parameters

 _sz_
  
> [in]変換される null で終わる文字列へのポインター。 有効な文字には、9 との両方の大文字と小文字の文字を 16 進数の文字 0 ~ f が含まれます。
    
 _pb_
  
> [out]返される 2 進数へのポインター。
    
 _cb_
  
> [in]_Pb_パラメーターのバイト単位のサイズです。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> 変換に成功しました。
    
MAPI_E_CALL_FAILED
  
> 無効な文字が発生しました。
    
## <a name="see-also"></a>関連項目



[FBinFromHex](fbinfromhex.md)

