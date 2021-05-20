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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439759"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
16 進数の文字列表現の指定された部分を 2 進数に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>パラメーター

 _sz_
  
> [in]変換する null 終端文字列へのポインター。 有効な文字には、0 ~ 9 の 16 進文字と、大文字と小文字の両方の文字 a ~ f が含まれます。
    
 _pb_
  
> [out]返されるバイナリ番号へのポインター。
    
 _cb_
  
> [in]  _pb_ パラメーターのサイズ (バイト単位)。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> 変換が成功しました。
    
MAPI_E_CALL_FAILED
  
> 無効な文字が検出されました。
    
## <a name="see-also"></a>関連項目



[FBinFromHex](fbinfromhex.md)

